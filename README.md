# Envanter & İmha Takip Sistemi

Bu proje, emanet bürolarında veya soruşturma işlemlerinde fiziksel envanterin (zarf, poşet, swap vb.) kayıt altına alınması, gruplanması ve imha süreçlerinin takibi için geliştirilmiş **mobil odaklı, hafif ve hızlı** bir web uygulamasıdır.

## 🚀 Proje Amacı
Yüzlerce emanet parçasının elle not edilmesinden kaynaklanan zaman kaybını ve veri hatalarını ortadan kaldırmak; tamamen tarayıcı tabanlı çalışarak kapalı sistemlerde dahi veri güvenliğini korumak amacıyla tasarlanmıştır.

## 🛠 Temel Özellikler
- **Mobil Öncelikli Arayüz:** Akıllı telefon ve tabletlerde seri giriş yapmak için optimize edilmiştir.
- **Mantıksal Gruplama:** Karar/Grup Yılı mantığı ile emanetleri raf/dosya düzenine göre ayırır.
- **Hızlı Seri Giriş:** Bir kez yıl seçimi yapıldığında, numaraları ardı ardına ekleyebileceğiniz akıcı bir giriş modu.
- **Dışa Aktarma:** Tek tıkla Excel (.xlsx) listeleme ve Yazıcı dostu (A4) PDF çıktı alma.
- **Çevrimdışı Çalışma:** İnternet gerektirmez, tüm veriler tarayıcınızın yerel hafızasında saklanır.
- **Güvenli Yedekleme:** JSON formatında veri yedekleme ve yükleme desteği.

## 🔒 Veri Güvenliği ve Gizlilik
Bu uygulama **"Local-First"** prensibiyle çalışır.
- **Sunucu Yok:** Verileriniz herhangi bir uzak sunucuya, veritabanına veya buluta gönderilmez.
- **Yerel Saklama:** Tüm kayıtlar sadece kullandığınız cihazın tarayıcısında (LocalStorage) saklanır.
- **Tam Kontrol:** "Verileri Yedekle" seçeneği ile verilerinizin tam bir kopyasını her zaman kendi bilgisayarınızda tutabilirsiniz.

## 💻 Kullanım Talimatları
1. **Giriş:** Uygulamayı tarayıcınızda açın.
2. **Grup Seçimi:** Üst kısımdaki akordiyon menüden ilgili Karar/Grup yılını seçin.
3. **Kayıt:** Emanet ve Soruşturma numaralarını girerek "Kaydet" butonuna basın.
4. **Kontrol:** "Liste" sekmesinden kayıtlarınızı görüntüleyin. İmha durumlarını tek tıkla güncelleyin.
5. **Rapor:** Sağ üstteki butonlarla Excel veya Yazdırma çıktısı alarak fiziksel dosya ile karşılaştırmanızı yapın.

## 📦 Kurulum ve Yayınlama
Bu uygulama statik HTML/JS yapısında olduğu için herhangi bir sunucu veya veritabanı kurulumu gerektirmez.
- **GitHub Pages / Cloudflare Pages:** Projenizi doğrudan bu platformlara yükleyerek herhangi bir hosting maliyeti olmadan anında canlıya alabilirsiniz.
- **Kurulum:** Sadece `index.html` dosyasını sunucunuza atmanız yeterlidir.

## 📄 Lisans
Bu proje geliştirme aşamasındaki, emanet büroları ve soruşturma takip işlemleri için özelleştirilmiş bir araçtır.

---
*İhtiyaç duyulması halinde geliştirilmeye ve özelleştirilmeye açıktır.*
