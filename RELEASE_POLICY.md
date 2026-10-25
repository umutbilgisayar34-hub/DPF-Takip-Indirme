# DPF Takip — Kararlı Sürüm Yayın Politikası

Bu herkese açık depo **yalnızca kullanıcı tarafından onaylanan, gerçek araçta doğrulanan ve yükleyici imzası uyumlu kararlı APK'leri** dağıtır. Deneme ve geliştirme sürümleri özel depoda kalır.

## Yayın için zorunlu kanıtlar

- **Kod/test:** Uygun Android derlemesi ve birim testleri başarılı; sürümün kaynak revizyonu kayıtlı.
- **Araç doğrulaması:** Yayımlanacak aynı sürüm Renault/Captur veya ilan edilen hedef araçta gerçek OBD ile sınanmış; ECU yanıtları, rejenerasyon uyarısı ve eksik parametreler dürüstçe raporlanmış.
- **Aynı APK:** Araçta test edilen **imzalı ikili dosyanın SHA-256 değeri** yayımlanan APK ile birebir aynı. Yeniden derleme yapıp eski test kanıtını kullanma.
- **Güncelleme ve veri bütünlüğü:** APK paket kimliği `tr.com.yigitbilgisayar.dpfpulse`; mevcut yüklemedeki imza ile eşleşme doğrulanmış. Eşleşmiyorsa kullanıcıyı mevcut kurulumunu kaldırmaya yönlendirme.
- **Onay:** Kamuya yayın için ayrı, açık, sürüme özgü onay verilmiş.
- **Dağıtım:** GitHub Releases varlıkları `DPF_Takip_vX.Y.Z_KARARLI.apk` ve `SHA256.txt`; yayımlanmış aynı etikette dosya değiştirilemez.

## Güvenlik / sorumluluk sınırları

- ECU'ya yazma, zorla rejenerasyon, DTC silme gibi işlemler bu DPF izleme sürümüne eklenmez.
- Üreticiye özel PID veya rejenerasyon algoritmaları araç üstünde doğrulanmadıkça standart PID olduğu iddia edilmez.
- Sıcaklık, basınç veya egzoz kokusu **tek başına ECU onaylı rejenerasyon kanıtı değildir**.
- Telemetri, VIN, GPS koordinatları, imzalama özel anahtarları ve özel kaynak kodlar herkese açık depoda tutulmaz.
- Uygulama tanı amaçlıdır; aracın kendi uyarıları ve üretici talimatları önceliklidir.

## DPF Takip v1.5.9 durumu

v1.5.9, ilk test ve derleme otomasyonundan geçmiştir ancak **gerçek araç üzerinde doğrulanmış kararlı sürüm değildir**. Eski kurulumlarla imza sürekliliği çözülmediğinden bu depoya normal güncelleme olarak yüklenmez. Geliştirme APK'sı, kararlı yayın standardını karşılayana kadar ayrı ve özel kalır.

## Korunan süreç

Ana geliştirme deposundaki sürüm yayın kontrolü; dosya SHA-256 kimliğini, önceki güvenilir imza sertifikasını, paket kimliğini, sürüm etiketini, araç üstü kabul kaydını ve açık yayın onayını denetler. Bu koşullardan herhangi biri yoksa yayın engellenir.
