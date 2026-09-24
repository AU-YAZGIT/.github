# Güvenlik Politikası

AÜ-YAZGİT depolarındaki kod, dokümantasyon ve altyapıların güvenliğini ciddiye alıyoruz. 

Bir güvenlik açığı bulduysan bize sorumlu bir şekilde bildirdiğin için teşekkür ederiz.

## Desteklenen Sürümler

Aksi belirtilmedikçe yalnızca her deponun **`main` dalındaki güncel hali** ve varsa **en son yayımlanan sürümü** güvenlik düzeltmesi alır.

Arşivlenmiş depolar için düzeltme yapılmaz.

## Güvenlik Açığı Bildirme

**Lütfen güvenlik açıklarını herkese açık issue, Pull Request veya Discussion olarak açma.** 

Açık ayrıntılar düzeltilmeden yayımlanırsa kullanıcılar risk altında kalabilir.

Bunun yerine şu yollardan birini kullan:

1. **GitHub özel bildirimi (tercih edilen):** İlgili deponun **Security** sekmesine git, **Report a vulnerability** düğmesini seç ve formu doldur. Bildirimin yalnızca depo yöneticilerine görünür.
2. **E-posta:** Düğmeyi göremiyorsan **[topluluk e-posta adresi]** adresine yaz. Konu satırına `[GÜVENLİK]` ve depo adını ekle.

### Bildirimde neler olmalı?

- Etkilenen depo, dosya veya sayfa
- Açığın türü (örn. sızdırılmış anahtar, bağımlılık açığı, yetkisiz erişim)
- Açığı yeniden üretmek için adımlar veya kanıt (kod, ekran görüntüsü)
- Olası etki
- Varsa çözüm önerin

## Bildirimden Sonra Ne Olur?

| Adım | Hedef süre |
| --- | --- |
| Bildirimin alındığının onayı | 7 gün içinde |
| İlk değerlendirme ve sonuç bilgisi | 14 gün içinde |
| Düzeltme veya çözüm planı | Açığın ciddiyetine bağlı |

Bu süreler garanti değil, hedeftir. Ekip gönüllülerden oluştuğu için gecikmeler olabilir. Yanıt alamazsan aynı kanaldan nazikçe tekrar yazabilirsin.

Açık giderildikten sonra, sen istersen, bildirimi yapan kişi olarak teşekkür kısmında anılırsın.

## Kapsam

**Kapsam içinde**
- AÜ-YAZGİT organizasyonundaki depolarda yer alan kod ve yapılandırmalar
- Depolarda yanlışlıkla paylaşılmış parola, API anahtarı, token veya kişisel veri
- Organizasyonun GitHub Actions iş akışlarındaki açıklar
- Topluluğun yönettiği web siteleri (yayında olanlar)

**Kapsam dışında**
- Ankara Üniversitesi'nin kendi sistemleri (üniversite portalı, bilgi işlem altyapısı vb.). Bunlar için üniversitenin Bilgi İşlem Dairesi ile iletişime geç.
- Üçüncü taraf hizmetler (GitHub, Kaggle vb.) kaynaklı açıklar. Bunları ilgili hizmete bildir.
- Sosyal mühendislik, fiziksel saldırı ve hizmet aksatma (DoS) testleri
- Otomatik tarayıcılardan gelen, doğrulanmamış raporlar

## Güvenli Test İlkeleri

Araştırma yaparken lütfen:
- Başkalarının verisine erişme, veriyi değiştirme veya silme
- Hizmetlerin çalışmasını aksatma
- Bulduğun açığı bildirimden önce başkalarıyla paylaşma
- Açığı gösterecek en az düzeyde test yap

Bu ilkelere uyarak ve iyi niyetle yapılan araştırmalar için hukuki işlem başlatmayı düşünmeyiz.

## Yanlışlıkla Gizli Bilgi Paylaştıysan

Bir depoya parola, API anahtarı veya token commit ettiysen:

1. **Önce anahtarı iptal et veya yenile.** Silmek yetmez, Git geçmişinde kalır.
2. Bize bildir ki geçmişten de temizleyelim.
3. Bir daha yaşanmaması için `.gitignore` ve ortam değişkenleri kullan.

## Katkı Verenler İçin

- Depolara hiçbir zaman gizli bilgi commit etme.
- Bağımlılıkları güncel tut ve Dependabot uyarılarını dikkate al.
- Güvenlik açığı düzelten PR'lar, açık ayrıntıları herkese açık göstermeden, önce bizimle özel olarak paylaşılmalıdır.

Ayrıca [Davranış Kuralları](https://github.com/AU-YAZGIT/.github/blob/main/CODE_OF_CONDUCT.md) ve [Katkı Rehberi](https://github.com/AU-YAZGIT/.github/blob/main/CONTRIBUTING.md) dosyalarına göz atmanı öneririz.