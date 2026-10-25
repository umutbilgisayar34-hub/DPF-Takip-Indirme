# DPF Takip — Resmî APK İndirme Alanı

Bu depo, **Yiğit Bilgisayar DPF Takip** Android uygulamasının yalnızca **onaylanmış kararlı APK sürümlerini** dağıtmak içindir.

> **Şu anda herkese açık kararlı APK yayımlanmadı.** Araç testi ve mevcut kurulumla imza uyumu doğrulanmayan geliştirme APK'leri burada paylaşılmayacak.

## APK indirme

Onaylı sürümler yayımlandığında [**Sürümler (Releases)**](../../releases) bölümünden `DPF_Takip_vX.Y.Z_KARARLI.apk` dosyasını indirebilirsiniz. Yanında bütünlük doğrulama için `SHA256.txt` bulunur.

Sürümler bölümü boşsa yayımlanmaya hazır bir kararlı APK henüz yoktur.

## Kurulum güvenliği

- **Mevcut DPF Takip uygulamasını kaldırmayın.** Kaldırma işlemi yerel sürüş raporları ve rejenerasyon geçmişini silebilir.
- Android'in mevcut kuruluma güncelleme yükleyebilmesi için APK'nın **paket kimliği ve imza sertifikası** önceki kurulumla uyumlu olmalıdır.
- `PARALEL_DENEME` ve diğer test APK'leri mevcut uygulamanın verilerinden ayrıdır; kararlı sürüm değildir.
- Rejenerasyon durumu ECU'dan doğrulanmamışsa sıcaklığa dayalı **olası rejenerasyon** uyarısı kesin ECU onayı anlamına gelmez.
- Bu yazılımın varlığı bir araçta bütün DPF PID'lerinin desteklendiğini veya her olayın yakalanacağını garanti etmez.

## Sürüm yayımlama kuralları

1. Birim testleri ve Android derlemesi başarılı olmalı.
2. Araç üstünde test edilip belirli APK adayının çalıştığı belgelenmeli.
3. Yayınlanacak **aynı dosyanın SHA-256 özeti**, paket kimliği, sürümü ve **imza sertifikası** doğrulanmalı.
4. Mevcut sürümlerle veri kaybı olmadan güncelleme uyumluluğu ayrıca doğrulanmalı.
5. Kararlı yayın açıkça onaylanmalı; hiçbir geliştirme derlemesi otomatik olarak kararlı sayılmamalı.

Ayrıntılar: [Yayın Politikası](RELEASE_POLICY.md).

## Özel geliştirme verileri

Kaynak kod, özel ECU ölçüm kayıtları, konum geçmişi, VIN, imzalama anahtarları ve kişisel bilgiler **bu herkese açık depoya konulmaz**. Geliştirme süreci özel depoda yürütülür.
