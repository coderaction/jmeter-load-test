# Load Test Nedir neden kullaniriz ?

Birim ve entegrasyon testleri kodun islevsel olarak dogru olmasini saglarken, yuk testi de ayni derecede onemli olan performansini olcer.Kodda ki darbagozin nerede oldugunu, uygulamanin verimli bir sekilde olceklenmesini, uygulamanin yanit verme suresinin ve veriminin ne oldugunu yuk testlerinde gorebiliriz.


## Ortamlarin kurulumu

- Daha once burada ki [repoda](https://github.com/coderaction/jmeter-first-run) jmeter'in nasil kurulacagini anlatmistim
- Ilgili repodan ornek kodlari clone'layip testleri gerceklestirebiliriz


## Apache Jmeter ile Test Plani olusturalim

Asagida ki apiler icin bir test plani olusturuyorum


| Url | Type |
| ------ | ------ |
| http://localhost:8080/students/list | [GET] List students |
| http://localhost:8080/students/id | [GET] Get student by id |
| http://localhost:8080/students/id | [GET] Get student by id |
| http://localhost:8080/students/id | [GET] Get student by id |
| http://localhost:8080/students/id | [GET] Get student by id |



Adim 1 - Test planına sağ tıklayın ve Add> Threads (Users)> Thread Group'u seçin. Bir test planında en az 1 Konu Grubu olmalıdır.

[![N|Solid](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/jmeter-add-plan.png)](https://nodesource.com/products/nsolid)

Daha sonra asagida ki gibi bir gorsel ile karsilasacaksiniz 


[![N|Solid](https://github.com/coderaction/jmeter-rest-api-load-test/blob/main/images/jmater-thread-group.png)](https://nodesource.com/products/nsolid)

