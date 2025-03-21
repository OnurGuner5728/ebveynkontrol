# Ebeveyn Kontrol Uygulaması

Bu proje, ebeveynlerin çocuklarının dijital aktivitelerini izlemelerine ve yönetmelerine yardımcı olan kapsamlı bir ebeveyn kontrol uygulamasıdır.

## Özellikler

- **Kullanıcı Yönetimi**: Kayıt, giriş, şifre sıfırlama, profil yönetimi
- **Cihaz Takibi**: Bağlı cihazların izlenmesi ve yönetimi
- **Konum İzleme**: Gerçek zamanlı konum takibi ve geçmiş hareket kayıtları
- **Uygulama Kullanım Analizi**: Kullanılan uygulamaların detaylı kullanım süreleri
- **Aktivite Akışı**: Çocukların dijital aktivitelerinin kronolojik görünümü
- **Bildirimler**: Önemli olaylar için anında bildirimler
- **Çok Dilli Destek**: Türkçe ve İngilizce dil desteği
- **PWA Desteği**: Mobil cihazlarda yerel uygulama gibi çalışabilme
- **Raporlama**: Detaylı kullanım raporları ve analizler

## Teknolojiler

- **Frontend**: React.js (TypeScript)
- **Backend/BaaS**: Supabase
- **Veritabanı**: PostgreSQL (Supabase üzerinde)
- **Kimlik Doğrulama**: Supabase Auth
- **Depolama**: Supabase Storage
- **Gerçek Zamanlı Veri**: Supabase Realtime
- **UI Tasarım**: Tailwind CSS
- **i18n**: react-i18next ile çoklu dil desteği
- **PWA**: Service Worker ve manifest.json

## Kurulum

1. Projeyi klonlayın:
   ```
   git clone https://github.com/yourusername/ebveynkontrol.git
   cd ebveynkontrol
   ```

2. Bağımlılıkları yükleyin:
   ```
   npm install --legacy-peer-deps
   ```
   Not: Bazı paket bağımlılık çakışmaları olabilir, bu durumda `--legacy-peer-deps` flag'ini kullanın.

3. `.env` dosyasını oluşturun ve düzenleyin:
   ```
   REACT_APP_SUPABASE_URL=your_supabase_url
   REACT_APP_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. Uygulamayı geliştirme modunda başlatın:
   ```
   npm start
   ```

## Proje Yapısı

```
src/
├── assets/          # Statik dosyalar (resimler, ikonlar)
├── components/      # Yeniden kullanılabilir UI bileşenleri
│   ├── auth/        # Kimlik doğrulama ile ilgili bileşenler
│   ├── common/      # Genel/ortak bileşenler
│   ├── devices/     # Cihaz yönetimi bileşenleri
│   ├── layout/      # Sayfa düzeni bileşenleri
│   └── settings/    # Ayarlar bileşenleri
├── constants/       # Sabit değerler ve yapılandırmalar
├── contexts/        # React Context API ile durum yönetimi
├── hooks/           # Özel React hook'ları
├── i18n/            # Çoklu dil desteği
├── pages/           # Sayfa bileşenleri
├── routes/          # Rota tanımları ve navigasyon
├── services/        # Harici servisler ve API işlemleri
├── supabase/        # Supabase istemcisi ve sorguları
├── types/           # TypeScript tip tanımlamaları
└── utils/           # Yardımcı fonksiyonlar ve araçlar
```

## Geliştirici Notları

### Bilinen Sorunlar ve Çözümleri

1. **Paket Bağımlılık Çakışmaları**:
   TypeScript versiyonu ile React paketleri arasında bağımlılık çakışmaları olabilir. Bu durumda, paket yüklerken `--legacy-peer-deps` veya `--force` bayrağını kullanın:
   ```
   npm install [paket-adı] --legacy-peer-deps
   ```

2. **react-intersection-observer Hatası**:
   Bu paketin yüklenmesi sırasında TypeScript versiyonu çakışması yaşanabilir. Çözüm:
   ```
   npm install react-intersection-observer --legacy-peer-deps
   ```

### Katkıda Bulunma

1. Bu repo'yu fork edin
2. Kendi feature branch'inizi oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some amazing feature'`)
4. Branch'inizi push edin (`git push origin feature/amazing-feature`)
5. Pull Request açın

## Lisans

Bu proje [MIT lisansı](LICENSE) altında lisanslanmıştır.

