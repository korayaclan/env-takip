# Emanet Envanter Sistemi v2

Emanet büroları ve soruşturma süreçlerinde fiziksel emanetlerin (zarf, poşet, swap vb.) saha kaydını hızlandırmak için geliştirilmiş **mobil odaklı, Local-First** web uygulamasıdır.

Kalem-kağıt ile yapılan kayıt işlemini ortadan kaldırır. Kayıtlar cihaz üzerinde tutulur, herhangi bir sunucuya veya buluta gönderilmez.

**Canlı uygulama:** [https://korayaclan.github.io/env-takip/](https://korayaclan.github.io/env-takip/)

---

## Amaç

İmha sürecinde olan yüzlerce emanet/envanter parçasının elle not edilmesinden kaynaklanan zaman kaybını ve veri hatalarını azaltmak.

Sistem özellikle şu iş akışına göre tasarlanmıştır:

1. Sahada hızlı dijital kayıt alınır
2. Grup bazlı A4 kontrol listesi yazdırılır
3. Memurlar UYAP üzerinden soruşturma / emanet numarası kontrolü yapar
4. İmha edilmeyecek emanetlerin türü basılı liste üzerine kalemle yazılır
5. İmha / İmha Değil kararı basılı listede işaretlenir

Yani sistem **dijital imha takip sistemi değildir**. Kayıt alma ve kontrol listesi üretme aracıdır.

---

## Temel Özellikler

### Mobil Öncelikli Arayüz
- Akıllı telefon ve tabletlerde hızlı kullanım için optimize edilmiştir
- Büyük dokunma alanları ve seri giriş odaklı form yapısı
- Gece / Gündüz modu

### Mantıksal Gruplama
- Karar Yılı (2005–2016) ve Raf / Grup (1B–80B) bazlı kayıt
- Bir kez yıl seçildikten sonra numaraları ardı ardına girebilme
- “Yok” seçeneği ile hızlı işaretleme

### Yazdırma / A4 Kontrol Listesi
- Her Karar Yılı / Raf Grubu için ayrı sayfalar
- Grup bazlı Sıra No. (sayfa değişince devam eder)
- Grup bazlı “Toplam Kayıt” bilgisi
- 35 satırlık A4 sayfalama
- İmha komisyonları için boş onay kutucukları (☐ İmha / ☐ İmha Değil)
- “Emanet Türü” alanı bilinçli olarak boş bırakılabilir (sonradan kalemle doldurulmak üzere)

### Veri Yönetimi
- Excel (.xlsx) dışa aktarma
- JSON formatında yedekleme ve geri yükleme
- Güvenli sıfırlama (önce yedek hatırlatması yapılır)
- Tüm veriler tarayıcı LocalStorage’ında tutulur

### Progressive Web App (PWA)
- Ana ekrana eklenebilir
- Standalone (adres çubuğu olmadan) açılabilir
- Temel Service Worker desteği mevcuttur

---

## Veri Güvenliği

Uygulama **Local-First** prensibiyle çalışır:

- Herhangi bir uzak sunucu veya veritabanı yoktur
- Veriler sadece kullandığınız cihazın tarayıcısında saklanır
- İstediğiniz zaman JSON yedeği alabilirsiniz
- Cihaz değiştiğinde veya tarayıcı verileri temizlendiğinde kayıtlar kaybolabilir — düzenli yedek almanız önerilir

---

## Kullanım

1. Uygulamayı tarayıcıda açın (tercihen mobil)
2. Üst kısımdan Karar Yılı ve Raf / Grup seçin
3. Emanet No ve Soruşturma / Esas No girerek kaydedin
4. Liste sekmesinden kayıtları kontrol edin
5. Excel veya Yazdır butonu ile çıktı alın
6. Basılı listeyi UYAP kontrolü sonrası kalemle tamamlayın

---

## Teknik Yapı

- Tek sayfa uygulama (HTML + Vue 3)
- Tailwind CSS
- SheetJS (Excel)
- Font Awesome
- LocalStorage
- Service Worker + Manifest (PWA)

Herhangi bir sunucu veya veritabanı kurulumu gerektirmez.  
GitHub Pages, Cloudflare Pages veya benzeri statik hosting’lerde çalışır.

---

## Sınırlamalar (Bilinçli Tasarım)

- Dijital imha durumu takibi yoktur
- Emanet türü zorunlu değildir (boş bırakılabilir)
- Yıllar ve raf grupları sabit listelerdir
- Offline çalışma, ilk yüklemeden sonra kısmen mümkündür (CDN bağımlılıkları nedeniyle tam garantili değildir)
- Veriler yalnızca bulunduğunuz tarayıcı / cihazda saklanır

---

## Kurulum

1. Repoyu klonlayın veya dosyaları indirin
2. `index.html` dosyasını herhangi bir statik sunucuya yükleyin
3. HTTPS üzerinden erişin (PWA için önerilir)

GitHub Pages kullanımı için repo ayarlarından Pages’i aktif etmeniz yeterlidir.

---

## Lisans

Bu proje emanet büroları ve soruşturma takip işlemleri için özelleştirilmiş, geliştirme aşamasındaki bir araçtır.  
İhtiyaç duyulması halinde geliştirilmeye ve özelleştirilmeye açıktır.