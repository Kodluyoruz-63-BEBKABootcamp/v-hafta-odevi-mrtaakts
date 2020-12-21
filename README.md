
# v-hafta-odevi

- DEVELOPER SUMMIT 2020'deki yazılım konferanslarından ilginizi çekenlerin özetlerini çıkarmaya çalışınız.

- SQLite ve LocalDB kavramlarını karşılaştırınız.

- Lazy Loading kavramı hakkında temel bir araştırma yapınız.

# DEV SUMMIT 2020 

Aşağıdaki 2 videoyu izledim ancak özetlerini çıkartamadım.

[Modern Web Development with Blazor & .NET 5](https://www.youtube.com/watch?v=CEjqhTGrqDY&list=PLdo4fOcmZ0oVWop1HEOml2OdqbDs6IlcI&index=5)
[High-performance Services with gRPC: What's new in .NET 5](https://www.youtube.com/watch?v=EJ8M2Em5Zzc&list=PLdo4fOcmZ0oVWop1HEOml2OdqbDs6IlcI&index=3)



# SQLite nedir ?

Sqlite, bir veritabanı kütüphanesidir. Kullanımı ve kurulumu oldukça kolaydır. Kullanmak için kurulum yapmanızı gerektirmez. Herhangi bir kurulum prosedürü yoktur. Kullanmak için herhangi bir sunucu işlemini başlatmak, durdurmak ya da yapılandırmak gerekmez. Sqlite kullanımı için bir yöneticinin yeni bir veritabanı örneği oluşturmasına veya kullanıcılara erişim izni vermesine gerek yoktur. Bir sistem çökmesi ya da elektrik kesintisinden sonra kurtarmak için herhangi bir eylem gerektirmez. Sadece çalışır. Hayat kolaylaştıran bir uygulamadır.

- SQLite’ın çalışması için herhangi bir sunucuya ihtiyacı olmadığı için, kurulum ve ya konfigürasyon adımları yoktur.
- Her veritabanı için sadece bir dosya vardır. Bu da veritabanının yedeklenmesini ve kopyalanmasını kolaylaştırır.
- Platform bağımsızdır.
- SQLite kompakttır. Tüm kütüphanenin boyutu 225kb’dır. Bazı özellikler çıkartılarak, bu boyut 170kb’a kadar indirilebilir. Bu sayede embedded ve ya symbian gibi platformlar için uygundur.

# LocalDB nedir ? 

Microsoft SQL Server Express LocalDB, geliştiricilere yönelik bir SQL Server Express özelliğidir. Gelişmiş Hizmetler içeren SQL Server Express'te mevcuttur.

LocalDB kurulumu, SQL Server Veritabanı Motorunu başlatmak için gereken minimum dosya kümesini kopyalar. LocalDB kurulduktan sonra, özel bir bağlantı dizesi kullanarak bir bağlantı başlatabilirsiniz. Bağlanırken, gerekli SQL Server altyapısı otomatik olarak oluşturulur ve başlatılır, bu da uygulamanın veritabanını karmaşık yapılandırma görevleri olmadan kullanmasını sağlar. Geliştirici Araçları, geliştiricilere, SQL Server'ın tam sunucu örneğini yönetmek zorunda kalmadan Transact-SQL kodunu yazmalarına ve test etmelerine olanak tanıyan bir SQL Server Veritabanı Motoru sağlayabilir.


## SQLite vs LocalDB

- Sqlite ve LocalDb genel projelerde mikrosaniyelik farklar yaratsa da , sadece sql amaçlı işlemlerde performans farkları ortaya koyulmaktadır. Aşağıda fotoğraflarını paylaştığım üzere sqlite genel olarak localdbden daha yavaş çalışmaktadır.


![1](https://www.diericx.net/images/embeddeddb1.png)

![2](https://www.diericx.net/images/embeddeddb2.png)

![3](https://www.diericx.net/images/embeddeddb4.png)


# Lazy Loading
Lazy Loading, sayfada yer alan bir ögenin ihtiyaç duyulmadığı takdirde çağrılmaması prensibi ile çalışır yani bir nesne örneğinin gerçekten ihtiyaç duyulacağı ana kadar alınmaması ve bekletilmesi amacıyla kullanılır. Bu yöntemde veriler sorguya bağlı olarak çekilir ve veri setinin içindeki tüm dataları yüklemek yerine kullanılacağı an tekrar sorgu atar ve veriyi çeker.

Bir entity'nin sub_entity'si olduğunda ve bu alt entity'nin çağırılmasının gerek olmadığı durumlarda kullanılır.

## Lazy Loading Avantajları

- İsteğe bağlı yükleme, zaman tüketimini ve bellek kullanımını azaltarak içerik dağıtımını optimize eder. Önce gerekli olan web sayfasının sadece bir kısmı yüklendiğinden, geçen süre daha az olur ve bölümün geri kalanının yüklenmesi gecikir, bu da depolamadan tasarruf sağlar. Tüm bunlar, istenen içerik anında beslendiğinden kullanıcı deneyimini geliştirir.

- Gereksiz kod yürütmeden kaçınılır.

- Zaman ve mekan kaynaklarının optimal kullanımı, onu iş adamları açısından uygun maliyetli bir yaklaşım haline getirir. (web sitesi sahipleri)
