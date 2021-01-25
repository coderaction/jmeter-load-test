# Load Test Nedir neden kullaniriz ?

Birim ve entegrasyon testleri kodun islevsel olarak dogru olmasini saglarken, yuk testi de ayni derecede onemli olan performansini olcer.Kodda ki darbagozin nerede oldugunu, uygulamanin verimli bir sekilde olceklenmesini, uygulamanin yanit verme suresinin ve veriminin ne oldugunu yuk testlerinde gorebiliriz.


## Ortamlarin kurulumu

- Daha once burada ki [repoda](https://github.com/coderaction/jmeter-first-run) jmeter'in nasil kurulacagini anlatmistim
- Ilgili repodan ornek kodlari clone'layip testleri gerceklestirebiliriz


## Apache Jmeter ile Test Plani olusturalim

Asagida ki apiler icin bir test plani olusturuyorum




## Adim 1

Test planına sağ tıklayın ve Add> Threads (Users)> Thread Group'u seçin. Bir test planında en az 1 Konu Grubu olmalıdır.

[![N|Solid](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/thread%20group.png?raw=true)](https://nodesource.com/products/nsolid)

Daha sonra asagida ki gibi bir gorsel ile karsilasacaksiniz 


[![N|Solid](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/jmater-thread-group.png)](https://nodesource.com/products/nsolid)


1 - Number of Threads(users) 50 kullanici olsun ve sisteme surekli olarak req gondersin 

> tekrar tekrar request gonderimi ancak bir once ki requestin responsu geldiginde gerceklesir

2 - Ramp-Up period (in seconds) Bunu tanimladigimizda maximum kullaniciya (1.de tanimladigimiz degere) kac saniye de ulasmak istedigini belirtmis oldugun alan oluyor

3 - Scheduler Configuration alaninda testin kac kez veya ne kadar sureyle calistirmak isteediginizi belirttiginiz bir alan bulunuyor 

## Adim 2

Neyin test edileceğini belirleyelim. ThreadGroup'a sağ tıklayın ve asagida ki islemi yapin. Yapilan bu islem sanki istegin kullanicidan gelmis gibi davranmasidir

[![N|Solid](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/jmater-thread-group.png)](https://nodesource.com/products/nsolid)

## Adim 3 

Artik bir api'ye post atma islemine gecebiliriz. Oncelikle asagida ki adimi uygulayalim;

[![N|Solid](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/login-jmeter.png)](https://nodesource.com/products/nsolid)

> burada onemli adimlardan birisi base url ile istek atilacak endpoint adresini ayirmaniz. Ornek vermem gerekirse 

https://www.milliyet.com.tr/pembenar/ bir endpoint'e get isteginde bulunmak istiyorsunuz 

Server Name or Ip: www.milliyet.com.tr 
Path Alanina: /pembenar

olarak yazmaniz gerekiyor 




