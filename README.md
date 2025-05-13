# Sohbet Uygulaması

Modern ve kapsamlı bir sohbet uygulaması. Next.js, React, Tailwind CSS ve Prisma kullanılarak geliştirilmiştir.

## Özellikler

- Kullanıcı Yönetimi
  - Kayıt ve giriş sistemi
  - Profil yönetimi (fotoğraf, biyografi, doğum tarihi, hobiler, iletişim bilgileri)
  - Cinsiyet bazlı eşleştirme sistemi

- Sohbet Özellikleri
  - Birebir sohbet
  - Fotoğraf paylaşımı
  - Ses mesajı gönderme
  - Görüntülü arama
  - Emoji desteği

- Abonelik Sistemi
  - Farklı abonelik paketleri
  - Premium özellikler
  - Ödeme entegrasyonu

- Güvenlik ve Gizlilik
  - Profil gizlilik ayarları
  - Mesaj şifreleme
  - Kullanıcı raporlama sistemi

- Ek Özellikler
  - Bildirim sistemi
  - Çevrimiçi/çevrimdışı durumu
  - Mesaj okundu bilgisi
  - Profil ziyaretçi takibi

## Teknolojiler

- Next.js 14
- React
- TypeScript
- Tailwind CSS
- Prisma
- PostgreSQL
- Socket.IO
- JWT Authentication

## Kurulum

1. Projeyi klonlayın:
```bash
git clone https://github.com/yourusername/sohbet.git
cd sohbet
```

2. Bağımlılıkları yükleyin:
```bash
npm install
```

3. Veritabanını oluşturun:
```bash
npx prisma migrate dev
```

4. .env dosyasını oluşturun:
```bash
cp .env.example .env
```

5. .env dosyasını düzenleyin ve gerekli değişkenleri ayarlayın.

6. Uygulamayı başlatın:
```bash
# Geliştirme modunda
npm run dev

# Socket.IO sunucusunu başlatmak için
npm run socket
```

5. Tarayıcınızda [http://localhost:3000](http://localhost:3000) adresini açın.

## Çevre Değişkenleri

`.env` dosyasında aşağıdaki değişkenleri ayarlayın:

```env
DATABASE_URL="postgresql://user:password@localhost:5432/sohbet"
JWT_SECRET="your-secret-key"
```

## API Endpoints

### Kimlik Doğrulama
- `POST /api/auth/register` - Kullanıcı kaydı
- `POST /api/auth/login` - Kullanıcı girişi

### Kullanıcılar
- `GET /api/users/search` - Kullanıcı arama
- `GET /api/users/[userId]` - Kullanıcı profili görüntüleme
- `PUT /api/users/[userId]` - Kullanıcı profili güncelleme

### Mesajlar
- `POST /api/messages` - Mesaj gönderme
- `GET /api/messages` - Mesajları getirme

### Arkadaşlık
- `POST /api/friends` - Arkadaşlık isteği gönderme
- `GET /api/friends` - Arkadaşlık isteklerini getirme
- `PUT /api/friends/[requestId]` - Arkadaşlık isteğini yanıtlama

### Abonelik
- `POST /api/subscriptions` - Abonelik oluşturma
- `GET /api/subscriptions` - Abonelik bilgilerini getirme

### Profil Ziyaretleri
- `POST /api/profile-visits` - Profil ziyareti kaydetme
- `GET /api/profile-visits` - Profil ziyaretlerini getirme

## Katkıda Bulunma

1. Bu depoyu fork edin
2. Yeni bir özellik dalı oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some amazing feature'`)
4. Dalınıza push edin (`git push origin feature/amazing-feature`)
5. Bir Pull Request oluşturun

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına bakın.
