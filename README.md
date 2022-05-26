# -week-1-assignment-mervecandan
JAVA 8, JAVA 11 VE JAVA 14 İLE GELEN YENİLİKLER
Java 8
Lambda expressions: Lambda expressionlar, herhangi bir class’a ait olmadan iş yapabilen fonksiyonlardır. Lambda ile birlikte Java, funtional programming dünyasına da girmiş bulunmaktadır. Bu oldukça önemli bir gelişme, Java’nın ilerde gideceği yol hakkında da ipucu veriyor bizlere. Lambda sayesinde hem daha okunabilir kod üretiyor, hem de kod tekrarından kurtuluyoruz. Bir lambda ifadesini tekrar tekrar kullanabilir, parametre olarak başka bir yere iletebiliriz.
(argument-list) -> {body}
argument-list : empty yada birden fazla olabilir duruma göre.
-> : arrow token, parametreler ile body statement’ı linkler.
{body} : expression yani asıl kodu içeren kısımdır.
fn(a, b)  -> { a+b; }  || fn(int a, int b)  -> { a+b; }  || fn(int a, int b)  -> { return a+b; } 

Functional interfaces: Tek bir abstract(soyut) methodu bulunan interface’ler için kullanılan tanımdır. Lambda ifadeleri ile sıkı bir ilişki içerisindedir. Ayrıca Single Abstract Method Interfaces (SAM Interfaces) olarak da bilinir. Functional interface’ler default ve static methodlar içerebilir ancak tek bir tane abstract methodu olmalıdır. Bunun nedeni de lambda ifadeleri ile çalışabilmesini sağlamaktır. 
Method references: Method references da yine lambda ve functional interface domaini ile gelen ve bir arada kullanılabilen özelliklerden biridir. 

Stream API: Stream API, Collection’lar üzerinde bazı işlemleri yapmayı kolaylaştıran bir yapıdır. Stream API sayesinde sık kullanılan çeşitli operasyonları yapabilirsiniz.
filter (filtreleme)
forEach (itere etme)
map (dönüştürme)
reduce (indirgeme)
distinct (tekil hale getirme)
limit (limitleme)
collect (toplama)
count (sayma)
min / max  (sıralama ile max-min eleman bulma
                   
Optional class: Java 8 ile birlikte gelen özelliklerden biri de bir objenin kullanılmadan önce yapılan null check’lerin daha okunabilir ve kontrol edilebilir olmasını sağlayan Optional yapısıdır. Optional class ile daha safe ve NPE almayan kod yazılabiliyor.  Objenizi Optional ile wrap ederek eğer null değilse kullan, null ise başka birşey yap diyebiliyorsunuz. Örneğin;

Java 11
Local-Variable Syntax for Lambda Parameters: Lambda ifadeler için yerel değişken kullanımı sağlar.
String API new Methods : String api sınıfına isBlank, lines, strip, repeat gibi faydalı methodlar eklendi.
Reading/Writing Strings to and from the File: Dosyadan string okuma ve dosyaya string yazma işlemlerini kolaylaştıran readString, writeString, isSameFile methodlarını sağlar.
Running Java File with single command: Dosyanın önce javac ile derlenip sonra java ile çalıştırılma gerekliliğini ortadan kaldırıp, dosyayı doğrudan java komutu ile çalıştırabilmeyi sağlar ve dolaylı olarak derler.

Java 14
Switch Expression Improvements: Switch ifadeleri daha da geliştirilerek JDK standardı haline getirilmiştir. Durum (case) başına birden çok sabite izin veren lambda ifadelerin kullanımını sağlar.
Data Classes: record: record anahtar sözcüğüyle declare edilen Data sınıfları , otomatik olarak getter/setter, constructor, equals() gibi standart methodlara sahip olarak bazı kod parçalarından kurtulmayı sağlar.
Pattern Matching for instanceof ( to check without Cast ): Nesnenin türünü kontrol etmek ve kullanmak için instanceof kontrolünün ardından cast özelliğini kullanmadan işlem yapmamızı sağlar.
Helpful NullPointerExceptions: Önceden, NullPointerException (NPE) için belirli bir sınıf ve satırda bazı değerlerin boş olduğu bildiriliyor ve hata ayıklaması-tespiti kabus olabiliyordu. Artık Java, belirli bir kod satırında tam olarak neyin-hangi verinin null olduğunu göstererek problemin kolayca çözülmesini sağlıyor.
