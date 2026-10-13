# SinyaFlix APK — nasıl derlenir (bilgisayara bir şey kurmadan)

1. github.com'da ücretsiz hesap açın ve **yeni bir depo (repository)** oluşturun (Private olabilir).
2. Bu klasörün **içindekileri** depoya yükleyin: *Add file → Upload files*.
   `.github` klasörü yüklenmezse: *Add file → Create new file*, ad olarak
   `.github/workflows/build-apk.yml` yazıp dosyanın içeriğini yapıştırın.
3. Üstteki **Actions** sekmesi → **Build APK** → **Run workflow**. Yaklaşık 5-10 dakika sürer.
4. Bittiğinde çalıştırmanın sayfasındaki **Artifacts → SinyaFlix-APK** dosyasını indirin,
   zip'ten çıkan `app-debug.apk` dosyasını telefona atıp kurun
   (Ayarlar'dan "bilinmeyen kaynaklardan yüklemeye" izin vermeniz gerekir).

Notlar
- Uygulama, `www/index.html` sayfasını sarar. Sayfayı değiştirip depoya yüklerseniz APK yeniden derlenir.
- Uygulama içinde istekler cihazın kendi ağ katmanından gittiği için tarayıcıdaki CORS ve
  http (düz) adres engeli burada geçerli değildir.
- Oynatma, telefondaki WebView'a bağlıdır; mkv/HEVC gibi bazı biçimler oynamayabilir.
