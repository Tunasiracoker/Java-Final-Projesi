Sinema Kayıt Sistemi

Bu proje, bir sinema müşteri kayıt ve yönetim sistemini içeren bir Java uygulamasıdır. Program, müşteri, film ve salon bilgilerini JSON dosyalarına kaydedip okuyabilir. Ayrıca salon doluluk durumu ve rezervasyon işlemleri gibi işlevleri de destekler.

Genel Özellikler

Müşteri Yönetimi: Yeni müşteriler ekleyebilir ve mevcut müşterileri listeleyebilirsiniz.

Film Yönetimi: Yeni filmler ekleyebilir ve JSON dosyasına kaydedebilirsiniz.

Salon Yönetimi: Salonları oluşturabilir, ekleyebilir ve doluluk durumlarını izleyebilirsiniz.

JSON Entegrasyonu: Veriler JSON formatında dosyalara kaydedilir ve okunur.

Konsol Etkileşimi: Kullanıcı menü üzerinden işlemleri gerçekleştirebilir.

Sınıf Yapısı

1. BaseEntity

Tüm nesnelerin ortak özelliklerini (id, createdAt) içerir.

bilgiGoster() metodu her türetilmiş sınıfta özelleştirilebilir.

2. Musteri

Amaç: Müşteri bilgilerini (ad, email) tutar.

Özellikler:

getAd(), getEmail(): Müşteri bilgilerini döndürür.

bilgiGoster(): Müşteri bilgilerini ekrana yazdırır.

3. Film

Amaç: Film bilgilerini (ad, sure, tur) tutar.

Özellikler:

getAd(), getSure(), getTur(): Film bilgilerini döndürür.

bilgiGoster(): Film bilgilerini ekrana yazdırır.

4. Salon

Amaç: Salon bilgilerini (isim, filmler, musteriler) yönetir.

Özellikler:

filmEkle(), musteriEkle(): Film ve müşteri ekler.

getFilmler(), getMusteriler(): Filmleri ve müşterileri döndürür.

bilgiGoster(): Salon bilgilerini ekrana yazdırır.

5. JsonHelper

Amaç: JSON dosyalarını okuyup yazmak için yardımcı işlevler sunar.

Metotlar:

writeToFile(String, List): Verileri JSON dosyasına yazar.

readFromFile(String, Class): JSON dosyasını okuyarak nesne listesine dönüştürür.

6. SinemaKayitSistemi

Ana sınıf, kullanıcı etkileşimlerini ve menü seçeneklerini içerir.

Menü İşlevleri

1. Yeni Müşteri Ekle

Kullanıcıdan müşteri bilgilerini (ad, email) alır.

Müşteriyi listeye ekler ve JSON dosyasına kaydeder.

2. Yeni Film Ekle

Kullanıcıdan film bilgilerini (ad, sure, tur) alır.

Filmi listeye ekler ve JSON dosyasına kaydeder.

3. Yeni Salon Ekle

Kullanıcıdan salon bilgilerini alır.

Salon listesine ekler ve JSON dosyasına kaydeder.

4. Verileri Listele

Müşteri, film ve salon bilgilerini JSON dosyasından okur ve ekrana yazdırır.

5. Çıkış

Programı sonlandırır.

JSON Dosyaları

Müşteri Dosyası (Musteri.json): Müşteri bilgileri JSON formatında saklanır.

Film Dosyası (Film.json): Film bilgileri JSON formatında saklanır.

Salon Dosyası (Salon.json): Salon bilgileri JSON formatında saklanır.

