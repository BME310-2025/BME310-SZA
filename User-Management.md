## 1. Sisteme Yeni Kullanıcı Kayıt Süreci
Kullanıcıların VolunteerHub platformuna kayıt olması aşağıdaki adımlarla gerçekleştirilir:
1. Ana sayfadan "Kayıt Ol" butonuna tıklanır.
2. Kayıt formu ekrana gelir ve kullanıcıdan aşağıdaki bilgiler istenir:
   - Ad ve Soyad
   - Geçerli bir E-posta Adresi
   - Şifre
   - Şifre Tekrarı (Doğrulama için)
   - Kullanıcı Türü (Gönüllü veya Organizasyon)
   - Telefon Numarası (Opsiyonel)
3. Kullanıcı Gizlilik Politikası ve Kullanım Şartları'nı onaylar.
4. "Kayıt Ol" butonuna basılarak form gönderilir.

## 2. Alınacak Bilgiler
- Ad ve Soyad (Zorunlu)
- E-posta Adresi (Zorunlu)
- Şifre ve Şifre Tekrarı (Zorunlu)
- Kullanıcı Türü Seçimi (Zorunlu)
- Telefon Numarası (Opsiyonel)

## 3. Doğrulama Adımları
- **E-posta Format Kontrolü:** E-posta adresinin geçerli formatta olması sağlanır.
- **Şifre Eşleşmesi:** Şifre ve Şifre Tekrarı alanlarının birebir aynı olması gerekir.
- **Şifre Güvenliği:** Şifrelerin minimum 8 karakter uzunluğunda ve hem harf hem rakam içermesi beklenir.
- **Zorunlu Alanlar Kontrolü:** Ad, soyad, e-posta ve şifre alanları boş bırakılamaz.

Başarılı bir kayıt işlemi sonrası kullanıcı giriş yapabileceği panele yönlendirilir.
## 4. Sisteme Kullanıcı Girişi Süreci
VolunteerHub platformunda kayıtlı kullanıcıların giriş yapabilmesi için aşağıdaki adımlar izlenir:
1. Ana sayfadan "Giriş Yap" butonuna tıklanır.
2. Kullanıcı giriş formunda aşağıdaki bilgileri doldurur:
   - E-posta Adresi
   - Şifre
3. "Giriş Yap" butonuna basılarak bilgiler sisteme gönderilir.

## 5. Şifreleme ve Doğrulama Süreci
- Kullanıcı şifreleri sistemde **hashlenmiş** (şifrelenmiş) şekilde saklanır. Şifreler düz metin (plaintext) olarak tutulmaz.
- Kullanıcının giriş yaparken girdiği şifre, aynı hash algoritması ile şifrelenerek sistemde saklanan hash değeriyle karşılaştırılır.
- E-posta adresi ve şifre doğru eşleşiyorsa kullanıcı giriş yapar.
- Yanlış bilgiler girilirse hata mesajı gösterilir ve yeni giriş denemesi istenir.

## 6. Güvenlik Adımları
- Şifreler güçlü olmalıdır (en az 8 karakter, harf ve rakam kombinasyonu).
- Çoklu başarısız giriş denemelerinde hesap geçici olarak kilitlenebilir (örneğin 5 başarısız denemeden sonra 15 dakika bloke).
- Giriş işlemleri SSL/TLS ile şifreli iletişim üzerinden gerçekleştirilir.
- Giriş yapan kullanıcılara güvenli oturum (session) kimlik doğrulaması uygulanır.
- Şüpheli giriş aktivitelerinde kullanıcıya bildirim gönderilir.

## 7. Kullanıcı Profil Bilgilerinin Düzenlenmesi
VolunteerHub platformunda kullanıcılar hesaplarına giriş yaptıktan sonra kendi profil bilgilerini düzenleyebilirler. Düzenleme adımları:
1. Kullanıcı ana panelde "Profilim" sekmesine tıklar.
2. Profil düzenleme sayfası açılır.
3. Kullanıcı aşağıdaki bilgileri güncelleyebilir:
   - Ad
   - Soyad
   - Telefon Numarası
   - Profil Fotoğrafı (Opsiyonel)

## 8. Şifre Güncelleme Süreci
- Kullanıcı profil düzenleme ekranında "Şifre Değiştir" seçeneğine tıklar.
- Mevcut şifresini girer.
- Yeni şifre ve yeni şifre tekrarı alanlarını doldurur.
- Yeni şifreler eşleşiyorsa ve minimum güvenlik şartlarını sağlıyorsa (en az 8 karakter, harf ve rakam kombinasyonu) sistem şifreyi günceller.
- Şifre başarıyla değiştirildiğinde kullanıcıya onay bildirimi gösterilir.

## 9. Profil Düzenleme Güvenlik Önlemleri
- Şifre güncelleme sırasında mevcut şifre mutlaka doğrulanır.
- Bilgiler güncellenmeden önce oturum doğrulaması yapılır (aktif login kontrolü).
- Şüpheli değişikliklerde kullanıcıya e-posta bildirimi gönderilir.

## Şifre Güçlendirme Gereksinimi

Kullanıcıların sisteme kaydolurken ve giriş yaparken kullandıkları şifrelerin en az 8 karakter uzunluğunda olması gerekmektedir.

Şifre güvenlik kriterleri:

- Minimum 8 karakter
- Büyük harf, küçük harf, rakam ve özel karakter kombinasyonu önerilir
- Zayıf şifreler sistem tarafından reddedilecektir
