# AÜ-YAZGİT Katkı Rehberi

AÜ-YAZGİT'e katkı vermek istediğin için teşekkürler!

Bu rehber, organizasyondaki tüm depolar için geçerli varsayılan kurallardır.

Bir deponun kendi `CONTRIBUTING.md` dosyası varsa, o depoda önce o dosya geçerlidir.

Katkı vermeden önce lütfen [Davranış Kuralları](https://github.com/AU-YAZGIT/.github/blob/main/CODE_OF_CONDUCT.md) dosyasını oku.

## İçindekiler

1. [Nasıl katkı verebilirim?](#1-nasıl-katkı-verebilirim)
2. [İş akışı](#2-iş-akışı)
3. [Adlandırma kuralları](#3-adlandırma-kuralları)
4. [Pull Request kuralları](#4-pull-request-kuralları)
5. [İnceleme süreci](#5-inceleme-süreci)
6. [İçerik politikası](#6-içerik-politikası)
7. [Atıf ve lisans](#7-atıf-ve-lisans)
8. [İçerik kaldırma talebi](#8-içerik-kaldırma-talebi)
9. [Güvenlik açığı bildirimi](#9-güvenlik-açığı-bildirimi)

---

## 1. Nasıl katkı verebilirim?

Kod yazmak zorunda değilsin. Şunların hepsi değerli katkıdır:

- Hata veya eksik bildirmek (issue açmak)
- Dokümantasyon, rehber veya ders notu yazmak ya da düzeltmek
- Yeni bir özellik, etkinlik veya proje fikri önermek
- Mevcut bir issue'yu üstlenip çözmek
- Başkalarının Pull Request'lerini incelemek

Başlamak için `good first issue` etiketli issue'lara bakabilirsin. Büyük bir değişiklik yapmadan önce mutlaka bir issue açıp konuş. Böylece emeğin boşa gitmez.

## 2. İş akışı

1. Depoyu kendi hesabına **fork**'la.
2. Fork'unu bilgisayarına klonla ve ana depoyu `upstream` olarak ekle:
   ```bash
   git clone https://github.com/<kullanici-adin>/<depo-adi>.git
   cd <depo-adi>
   git remote add upstream https://github.com/AU-YAZGIT/<depo-adi>.git
   ```
3. Çalışmaya başlamadan önce fork'unu güncelle:
   ```bash
   git checkout main
   git pull upstream main
   ```
4. Yeni bir dal aç (adlandırma için [bölüm 3](#3-adlandırma-kuralları)):
   ```bash
   git checkout -b docs/katki-rehberi-duzeltmesi
   ```
5. Değişikliklerini yap, küçük ve anlamlı commit'lere böl.
6. Dalını fork'una gönder:
   ```bash
   git push origin docs/katki-rehberi-duzeltmesi
   ```
7. Ana depoya **Pull Request (PR)** aç.

> `main` dalına doğrudan push yapılmaz. Tüm değişiklikler PR ile gelir.

## 3. Adlandırma kuralları

### Dallar (branch)

`tur/kisa-aciklama` biçiminde, küçük harf ve tire ile yazılır.

| Tür | Ne için | Örnek |
| --- | --- | --- |
| `feat/` | Yeni özellik | `feat/datathon-basvuru-formu` |
| `fix/` | Hata düzeltme | `fix/kirik-baglanti` |
| `docs/` | Dokümantasyon | `docs/git-workshop-anlatimi` |
| `content/` | Not, materyal, workshop içeriği | `content/goruntu-isleme-hafta3` |
| `chore/` | Bakım, ayar, bağımlılık | `chore/gitignore-guncelle` |

### Commit mesajları

Commit mesajlarında [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) standardını takip ediyoruz. 

Standardın tamamı için bağlantıya bakabilirsin. 

Kısaca biçim şöyledir:

```
tur: kısa açıklama
```

Örnekler:

```
feat: datathon başvuru formu ekle
fix: README'deki kırık bağlantıyı düzelt
docs: Git workshop anlatımını genişlet
```

Kurallar: açıklama küçük harfle başlar, sonuna nokta konmaz, tek bir değişikliği anlatır.

### Depo, klasör ve dosya adları

- **Depo adları:** küçük harf, kelimeler tire ile ayrılır, İngilizce veya Türkçe olabilir ama Türkçe karakter içermez (örn. `notes-from-students`, `hosgeldin-kiti`).
- **Klasör ve dosya adları:** Türkçe karakter ve boşluk kullanma. Kelimeleri `_` veya `-` ile ayır. Depo içinde tek bir biçim seç ve sürdür.
  - Doğru: `Hafta3_Bagli_Listeler.md`
  - Yanlış: `hafta 3 bağlı listeler.md`
- Dokümanların **içeriği** Türkçe karakterlerle, UTF-8 olarak yazılır.

## 4. Pull Request kuralları

- Bir PR tek bir konuyu ele almalı. Küçük PR'lar hızlı incelenir.
- Başlık, commit biçimiyle aynı olmalı (`docs: katkı rehberini güncelle`).
- Açıklamada şunları yaz: **ne** değiştirdin, **neden**, ilgili issue varsa **`Closes #12`**.
- Görsel bir değişiklik varsa ekran görüntüsü ekle.
- PR şablonundaki kutucukları doldur.
- İşin henüz bitmediyse **Draft PR** olarak aç.
- Değişikliği yapmadan önce çakışmaları çöz; PR'ın güncel `main` ile uyumlu olmalı.
- **Kendi PR'ını kendin birleştirme.**

## 5. İnceleme süreci

- Her PR en az **1 onay** almalı; onay veren PR sahibi olamaz.
- Eğer depoda PR onaylama yoksa Proje sahibi kişi veyahut Proje ekibi değerlendirebilir.
- Hedefimiz, ilk yanıtı **7 gün** içinde vermektir. Bu süre garanti değil, hedeftir; bekliyorsan nazikçe PR'ın altına yorum yazabilirsin.
- İnceleyenler şuna bakar: doğruluk, okunabilirlik, bu rehbere ve [içerik politikasına](#6-i̇çerik-politikası) uygunluk, ilgili konunun kapsamına uyum.
- Değişiklik istenirse aynı dala yeni commit ekle; PR otomatik güncellenir.
- Beklenen düzeltme **30 gün** içinde gelmezse PR kapatılabilir. İstediğin zaman yeniden açabilirsin.
- Anlaşmazlık olursa son karar ilgili deponun sorumlusuna, o da çözemezse yönetim kuruluna aittir.

## 6. İçerik politikası

Aşağıdaki kurallar özellikle ders notu, workshop materyali ve benzeri içerikler için geçerlidir.

**Yükleyebilirsin**
- Kendi hazırladığın notlar, özetler, kod ve çizimler
- Açık lisanslı kaynaklardan, lisans şartlarına uyarak aldığın içerikler
- Kaynak göstererek yaptığın kısa alıntılar

**Yükleyemezsin**
- Kitap veya makale sayfalarının taranmış veya kopyalanmış halleri
- Öğretim üyesinin **izni olmadan** ders slaytları veya ders materyalleri
- Devam eden sınavlara ait sorular, cevaplar veya kopya işlevi gören içerikler
- Başkasına ait kişisel bilgiler (isim, numara, e-posta, fotoğraf)
- Başkasının çalışmasını kendi çalışmanmış gibi sunan içerik
- Nefret söylemi, taciz veya yasa dışı içerik
- Parola, API anahtarı, token gibi gizli bilgiler

**Yapay zeka ile üretilen içerik**
- Kullanabilirsin ama içeriği **kendin doğrulamalı ve düzenlemelisin.**
- PR açıklamasında yapay zeka kullandığını belirt.
- Doğruluğundan emin olmadığın içerik gönderme.

**Dosya boyutu**
- Tek dosya için üst sınır **10 MB**'tır. Daha büyük dosyalar için önce issue aç.
- Görselleri, ilgili notun yanında `images/` veya `assets/` klasörüne koy.
- Notlar için `.md` veya `.pdf` tercih edilir. Derlenmiş çalıştırılabilir dosyalar (`.exe` vb.) kabul edilmez.

**Alternatif Yol**
- Eğer depo içerisinde dosyaları yüklemek istemezsen kendi deponu aç ve profilinde sergile. Bizim açtığımız depo sadece bir giriş noktası olur ve öğrenciler senin depondan fayda eder.

## 7. Atıf ve lisans

- Notların başına kısa bir üst bilgi ekle:
  ```yaml
  ---
  ders: Görüntü İşleme
  donem: 2026 Güz
  yazar: Kullanıcı Adı  # takma ad kullanabilirsin
  kaynaklar:
    - Ders kitabı adı, yazar, yıl
  ---
  ```

- Başkasına ait fikir, şekil veya kod kullandıysan kaynağını belirt.
- Katkıların, ilgili deponun `LICENSE` dosyasındaki lisansla yayımlanır. Bunu kabul etmiyorsan katkı göndermemelisin.
- Katkı verenler `Contributors` listesinde ve gerektiğinde proje sayfasında anılır.
- Projelerin akademik yayına dönüşmesi halinde, emeği geçen öğrenciler proje sahibi olarak yer alır; danışman akademisyenler ortak yazar olarak desteklenebilir. Ayrıntılar ilgili projede önceden konuşulmalıdır.

## 8. İçerik kaldırma talebi

Bir öğretim üyesi, öğrenci veya hak sahibi olarak içeriğinin kaldırılmasını istiyorsan:

1. İlgili depoda **"İçerik Kaldırma Talebi"** şablonuyla issue aç **veya** proje komitesi ile iletişime geç.
2. Hangi dosya veya içeriğin kaldırılmasını istediğini ve nedenini belirt.
3. Talebe **7 gün** içinde yanıt vermeyi hedefliyoruz. Hak sahibinin talebi netse içerik önce **geçici olarak kaldırılır**, sonra değerlendirme yapılır.

Kişisel bilgi veya telif ihlali içeren bir içerik görürsen, herkese açık issue yerine direkt bizimle iletişime geçerek ile bildirmeni öneririz.

## 9. Güvenlik açığı bildirimi

Bir güvenlik açığı bulduysan lütfen **herkese açık issue açma**. [SECURITY.md](https://github.com/AU-YAZGIT/.github/blob/main/SECURITY.md) dosyasındaki adımları izle.

## Sorularınız mı var?

- Genel sorular için deponun **Discussions** sekmesini kullan.
- Diğer konular için bize ulaş.

Katkıların için şimdiden teşekkürler!
