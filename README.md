Proje Businessı : Bu proje ne yapar kapasamı ve amacaı nedir? 
Öğrenci yoklama sistemi :Amaaç öğrenciler'in girdikleri yada giremdeikleri dersin listesini oluşturma
Kulanılan Mimari : Katmanlı mimari 
Circular Dependency

Kullanılan Kütüphaneler 
-ORM
 -EntityFrameworkCore
 -EntityFrameworkCore.Relational
 -EntityFrameworkCore.Tools
-Database
 -EntityFrameworkCore.PostgreSQL

-Validasyon
 FluentValidation
 Girilen verileri,requestleri validate etmek içim ullanılır,Merkezi doğrulama,kolay test edilebilir,hata mesjalrını özelleştirme

-MediatR-CORS(Command Query Responsibility)
  MediatoR Datnet kütüphaneleri için kullanılıp Cors ve mediator tasarım deseninin uygulamaya yarar
  Sınıflar arasında bağımlılığı azaltıp,bileşenler arası iletişimi merkezi bir mekanizma aracılığıyle yönetmemizi sağlar
  CORS
  Command : Veri tabanında değişklikik yapan işlemler 
  Query   : Veri tabanından okuma yapan işlemler


-Swagger Dökümantasyon
 Swashbuckle-swagger entegrasyonu için 

-Authentication(Kimlik doğrulama)
 JWTBearer Token
 Authentication.JwtBearer

 -Authentication-Kimlik doğrulama-Sisteme giren kişinin kim olduğunu belirleme süreci
 Kulllanıcı adı ve parola ile sisteme girenin kim olduğuna karar veriyorum
 Kontrol ettiğimiz      metod -sign-in
 Kullanıcı adı(eposta) ve şifre verme -sing-up(Register,kaydetme):sistemi kullanacaklara kullanıcı ade ve şifre belirleme metodu
  Authorization 
   -Normal Authorization : email ve password ile giriş
   -2FA(iki faktörlü kimlik doğrulama) Notmal Authorizationa ek olarak bir code bilgisi ile(öreneğim emal'e yada Telefona'a gelen) kimlik doğrulama yapılabilir

Authantication Yöntemleri 
 Kullanıcı adı ve şifre
 Biometrik doğrulama(parmak izi,yüz tanıma)
 2FA-Two Factor

 -Authorization(Yetkilendirme)
  Kimliği doğrulanan kullanıcı hangi kaynkalara(endointlere) erişecek bunu belirleme işlemdir
  Kullancının sahip olduğu roller ve izinlerin yönetilmesidir
  Kullanıcı sisteme girdikten sonra sadece kendi mesajlarını görebilir,diğer kullanıcılara gelen mesajları göremez
  Sisteme kullanıcı ekleme(register,sign up) ,silme işleminin belirlik kişilerde olması 

  Authorization Yönetmleri 
  -Role-Base Authorization 
   -Rollere erişebileceği yetkiler tanımlanır,Kullanıcılarada roller atanır 
   Role-admin
   Role-basic
   tuğçe-basic
   esra-admin
   1)Role tanımla
   2)Role yetki verme
   3)Kullanıcının role bağlanması
  -Plicy-based Authorization 
   kullanıcının belirli özellik veya durumuna göre izin beirleme,sadece kadınlar bu işlemleri yapsın
  -Claim-based Authorization kullanıcının belirli taleplerine göre izinler tanımlanır 
   Departman bazlı yetki düzenleme 

-Ardalis.Specification
-Ardalis.Specification.EntityFrameworkCore
 
-Ardalis.Specification 
  Bir specification Pattern uygulamasıdır,Belirli bir kriteri karşılayan nesneleri tanımlayan yeniden kullanılabilir ve test edilebilir sınıflar
  Yeniden kullanılabilirlik,Test edilebilme,kod tekrarını azaltma

-Ardalis.Specification.EntityFrameworkCore
 Ardalis kütüphanesini Enity Framework Core ile entegre eder.Bu Entegrasyon EF ile çalışan veri eirşim katmanlarında Specification'ı kullanmamızı sağlar

 -Mapper
  AutoMapper
  AutoMapper.Extensions.Microsoft.DependencyInjection

  AutoMapper :Nesneler arası dönüşüm yapmayı kolaylaştırmak için kullanılır,AutoMapper verilen nesnler arasında 
  otamatik bir şekilde dönüşüm yapar ve manuel mapping'e göre kod daha temiz ve düzenli olur

  DTOs :Veri taşıyan nesneler 
  Entity to DTOs
