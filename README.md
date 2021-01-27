# Bu yazi dizisi 3 bolumden olusmaktadir

- Jmeter nasil calistirilir ? [Repo](https://github.com/coderaction/jmeter-first-run) 
- Jmeter bir endpoint'e nasil istek gonderilir? [Repo](https://github.com/coderaction/jmeter-rest-api-load-test) 
- Jmeter Auth token kullanilan bir endpointte token alinip diger apilere nasil otomatik bir sekilde verilir?  

# Load Test Nedir neden kullaniriz ?

Birim ve entegrasyon testleri kodun islevsel olarak dogru olmasini saglarken, yuk testi de ayni derecede onemli olan performansini olcer.Kodda ki darbagozin nerede oldugunu, uygulamanin verimli bir sekilde olceklenmesini, uygulamanin yanit verme suresinin ve veriminin ne oldugunu yuk testlerinde gorebiliriz.

## Apache Jmeter ile Test Plani olusturalim

Simdi adim adim bir endpoint'e post atmayi deneyelim...


## Adim 1

Test planına sağ tıklayın ve Add> Threads (Users)> Thread Group'u seçin. Bir test planında en az 1 Konu Grubu olmalıdır.

[![](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/thread%20group.png?raw=true)]()

Daha sonra asagida ki gibi bir gorsel ile karsilasacaksiniz 


[![](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/jmater-thread-group.png)]()


1 - Number of Threads(users) 50 kullanici olsun ve sisteme surekli olarak req gondersin 

> tekrar tekrar request gonderimi ancak bir once ki requestin responsu geldiginde gerceklesir

2 - Ramp-Up period (in seconds) Bunu tanimladigimizda maximum kullaniciya (1.de tanimladigimiz degere) kac saniye de ulasmak istedigini belirtmis oldugun alan oluyor

3 - Scheduler Configuration alaninda testin kac kez veya ne kadar sureyle calistirmak isteediginizi belirttiginiz bir alan bulunuyor 

## Adim 2

Neyin test edileceğini belirleyelim. ThreadGroup'a sağ tıklayın ve asagida ki islemi yapin. Yapilan bu islem sanki istegin kullanicidan gelmis gibi davranmasidir

[![](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/jmater-thread-group.png)](https://nodesource.com/products/nsolid)

## Adim 3 

Artik bir api'ye post atma islemine gecebiliriz. Oncelikle http requeset page olusturmamiz gerekiyor,

[![](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/httpRequesetJmeter.png)]()

 Olusturmus oldugumuz http request uzerinden artik post islemleri gerceklestirebiliriz
 burada onemli adimlardan birisi base url ile istek atilacak endpoint adresini ayirmaniz. Ornek vermem gerekirse 

https://www.milliyet.com.tr/pembenar/ bir endpoint'e get isteginde bulunmak istiyorsunuz 

Server Name or Ip: www.milliyet.com.tr 
Path Alanina: /pembenar

olarak yazmaniz gerekiyor ornek olarak 

[![](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/http-request.png)]()

Eğer benim gibi Body JSON gönderiyorsanız. Test Plan >Add > Config Element > HTTP Header Manager oluşturup “Content-Type” olarak application/json girin.

[![](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/httpheadermanager.png)]()

[![](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/httpHeaderManagercontentType.png)]()

## Adim 4 

Artik islemlerimiz tamam requeest gonderip responslari alabilirz, responslari alip analiz edebilmemiz icin Thread Group Listener’lar eklememiz gerekiyor.

- Aggregate Graph
- View Result in Table
- View Results Tree gibi…

> bu repo icerisinde bulunan jmx uzantili dosya aslinda yukari da hazirlamis oldugumuz yapinin kaydedilmis halidir, sizde jmter'i calistirip open diyerek bu dosyayi acabilir dogrudan kullanabilirsiniz.

### Todos
 - Thread Group Listener tiplerini bir arkadas anlatabilirse sevinicem.
 - Online bir endpoint bulunup (ibb endpointleri olur) jmx dosyasi duzenlenebilir
 - Jmeter ile sonuclari nasil yorumlariz yazilmasi gerekiyor



