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

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
