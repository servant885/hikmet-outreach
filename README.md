# Hikmet Outreach

GitHub Pages üzerinde çalışan kişisel, manuel onaylı YouTube cevap asistanı.

## Kurulum
1. GitHub'da yeni repo açın. index.html ve app.js dosyalarını köke yükleyin. Settings > Pages > Deploy from a branch > main / root seçin.
2. Google Cloud Console'da proje oluşturun, YouTube Data API v3 etkinleştirin. API anahtarı oluşturun; YouTube API ve kendi site adresinizle kısıtlayın.
3. Google Auth Platform üzerinden OAuth consent screen yapılandırın. Test modunda kendi hesabınızı test kullanıcısı ekleyin. Web application OAuth client oluşturun. Authorized JavaScript origins alanına https://KULLANICI.github.io yazın (repo yolu olmadan). YouTube force-ssl kapsamı gerekir. Google'ın hesap yaş ve izin koşulları geçerlidir.
4. Google AI Studio üzerinden Gemini API anahtarı alın (hesap uygunluğu ve bölge koşullarına tabidir). Kullanılabilir model adını girin. API anahtarını repoya koymayın.
5. Siteyi açın, bilgileri girin, Google hesabını bağlayın, video linkini girin. Her yorum için değerlendirme düğmesine basın. Taslağı kontrol edin ve yalnızca uygun olanı yayınlayın.

## Sınırlar ve güvenlik
- Bu sürüm yorumları sayfa sayfa getirir; AI değerlendirmesi kullanıcı tarafından yorum başına başlatılır. Otomatik toplu analiz veya gönderim yoktur. Yalnızca üst düzey yorumlar okunur.
- Anahtarlar ve erişim tokeni sayfa belleğinde tutulur, kalıcı depolama yoktur. Tarayıcıda kullanılan anahtarlar gizli sunucu anahtarı sayılmaz. Kişisel kullanım içindir; herkese açık çok kullanıcılı kullanımda sunucu tarafı proxy gerekir.
- Seçilen yorum metni Gemini hizmetine gönderilir. Hassas kişisel bilgi içeren yorumları göndermeyin. YouTube ve Gemini koşullarına uyun. Spam, tekrar eden mesajlar ve istenmeyen dini baskıdan kaçının.
- Ücret ve kotalar sağlayıcıya bağlıdır. Google OAuth doğrulaması gerekebilir. Model kullanılabilirliği değişebilir.
- Gerçek API çağrıları ve OAuth akışı hesap bilgileri olmadan test edilmemiştir. Bu bir başlangıç sürümüdür.
