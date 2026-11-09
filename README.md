# Keskin · Berber Defteri

Keskin, berber dükkânının günlük işlerini telefondan takip etmek için hazırlanmış mobil uyumlu bir web uygulaması prototipidir. Randevu, kasa, veresiye, müşteri kartları ve çırak ödemelerini tek ekranda toplar.

> Bu proje şu an tarayıcıda çalışan tek kullanıcılı bir prototiptir. Veriler cihazın tarayıcısında saklanır; farklı cihazlar arasında otomatik eşitlenmez. Gerçek müşterilerle kullanmadan önce yedek alın ve uygulamayı HTTPS üzerinden yayınlayın.

## Özellikler

- **Randevu:** Gün ve saat seçme, hizmet ve ücret belirleme, çalışan seçme, randevu durumunu değiştirme.
- **Sesli randevu:** Desteklenen tarayıcılarda Türkçe konuşmayı yazıya çevirerek randevu oluşturma. Tarayıcı mikrofon izni ister; bazı telefonlarda veya dosyayı doğrudan açınca ses tanıma kullanılamayabilir.
- **Kasa:** Günlük para girişi ve çıkışı ile nakit/kart hareketlerini kaydetme.
- **Veresiye:** Müşteri bakiyelerini izleme ve alınan ödemeleri kaydetme.
- **Müşteri kartları:** Telefon numarası, randevu geçmişi ve açık bakiyeyi görme; müşteri arama.
- **Çırak hesabı:** Haftalık ücret, avans ve ödemeleri takip etme.
- **Ayarlar:** Hizmetleri, fiyatları, çalışma saatlerini ve randevu aralığını düzenleme.
- **Yedekleme:** Verileri JSON dosyasına indirme ve daha sonra dosyadan geri yükleme.
- **Telefona ekleme:** PWA manifesti ve service worker içerir. HTTPS ile yayınlandıktan sonra desteklenen tarayıcılarda ana ekrana eklenebilir.

## Başlama

1. Bu depodaki **Code → Download ZIP** seçeneğiyle projeyi indirin veya dosyaları bilgisayarınıza alın.
2. Hızlı önizleme için `index.html` dosyasını tarayıcıda açın.
3. Uygulamayı telefona yüklenebilir şekilde kullanmak için dosyaları HTTPS destekleyen bir statik site barındırma hizmetine yayınlayın.
4. Yayındaki siteyi telefonda açın. iPhone’da Safari paylaşım menüsünden **Ana Ekrana Ekle**; Android’de Chrome menüsünden **Ana ekrana ekle** seçeneğini kullanın.
5. İlk açılışta görünen örnek kayıtları inceleyin. Kendi işletme bilgilerinizi Ayarlar bölümünden girin.

## Dosyalar ne işe yarıyor?

| Dosya | Görevi |
| --- | --- |
| `index.html` | Uygulamanın ekranları, tasarımı ve tarayıcıda çalışan işlevleri |
| `manifest.webmanifest` | Uygulama adı, renkleri ve ana ekrana ekleme bilgileri |
| `keskin-icon.svg` | Uygulamanın makas simgesi |
| `sw.js` | Uygulama çevrimdışı kullanımına yönelik önbellek altyapısı |

## Veriler ve gizlilik

Kayıtlar `localStorage` ile o tarayıcıda ve cihazda tutulur. Tarayıcı verilerini silmek kayıtları silebilir. Yedek dosyasını güvenli bir yerde saklayın. Yedeği geri yüklemek o anki kayıtların yerine geçer. Birden fazla berberin ortak kullanımı, çevrimiçi eşitleme, hesap sistemi veya sunucu tarafında saklama bu prototipte bulunmaz.

## Geliştirme notu

Uygulama HTML, CSS ve JavaScript ile hazırlanmıştır; kurulum için paket yöneticisi veya derleme adımı gerekmez. GitHub Pages gibi HTTPS yayınlama yöntemiyle barındırılabilir. Mikrofonla konuşmayı yazıya çevirme özelliği tarayıcı desteğine bağlıdır.

## Lisans

Bu depoya henüz açık kaynak lisansı eklenmemiştir. Lisans eklenene kadar kodu kullanma, değiştirme ve dağıtma koşulları ayrıca belirlenmiş değildir.
