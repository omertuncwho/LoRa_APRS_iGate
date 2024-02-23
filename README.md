#### Bu çeviri, Türk radyo amatörlerinin anadilinde daha kolay erişebileceği bir kaynağın oluşturulmasını amaçlamaktadır.

# LoRa APRS iGate

[![Integration Tests](https://github.com/lora-aprs/LoRa_APRS_iGate/actions/workflows/build_check.yml/badge.svg)](https://github.com/lora-aprs/LoRa_APRS_iGate/actions/workflows/build_check.yml)

LoRa APRS iGate, Amazon, eBay veya AliExpress'ten satın alabileceğiniz çok ucuz donanımlarla çalışacaktır. Deneyin ve APRS ağına katılın.

![TTGO LoRa32](pics/iGate.png)

## Diğer Amatörlerden Blog Gönderileri ve YouTube Videoları

* [Manuel Lausmann - iGate & Tracker](https://www.youtube.com/watch?v=-KdFQEaNC1k) (YouTube - Almanca) 04.06.2021
* [Manuel Lausmann - Installationsanleitung als PDF](http://mala-one.de/Lora-APRS/) (PDF - Almanca) 04.06.2021
* [OE1ROT](https://www.aronaut.at/2020/11/lora-aprs-gateway-mit-esp32-boards/) (Blog yazısı - Almanca) 14.11.2020
* [DL7AG](http://online.dl7ag.de/lora-aprs-dl7ag-10/) (Blog yazısı - Almanca) 08.11.2020
* [Manuel Lausmann - iGate](https://www.youtube.com/watch?v=C7hfVe32pXs) (YouTube - Almanca - OLD) 06.11.2020
* [Manuel Lausmann - Tracker](https://www.youtube.com/watch?v=clIlTEFbWLk) (YouTube - Almanca - OLD) 02.11.2020
* [OE1ROT](https://www.aronaut.at/2019/12/lora-aprs-tracker-mit-ttgo-t-beam-433mhz/) (Blog yazısı - Almanca) 09.12.2019

Kendi bilgilerinizi ekleyin veya eklenmek istiyorsanız bir bilet oluşturun.

## Supported boards

Herhangi bir değişiklik yapmadan bir Lora32 kartından birini kullanabilirsiniz:

* Heltec WiFi LoRa 32 V1 (433MHz SX1278)
* Heltec WiFi LoRa 32 V2 (433MHz SX1278)
* TTGO LoRa32 V1 (433MHz SX1278)
* TTGO LoRa32 V2 (433MHz SX1278)
* TTGO LoRa32 V2.1 (433MHz SX1278)
* TTGO T-Beam V0.7 (433MHz SX1278)
* TTGO T-Beam V1 (433MHz SX1278)
* Tracker D from [OE1ACM and OE1CGC](https://www.lora-aprs.at/)
* ve tabii ki daha fazlası...

İşte bazı örnek kartlar için amazon-de bağlantıları:
* [LoRa32 V1](https://www.amazon.de/dp/B07VPHYYJD)
* [LoRa32 V1](https://www.amazon.de/dp/B07QRG89ZV)
* [LoRa32 V2](https://www.amazon.de/dp/B07VL97VNH)
* [LoRa32 V2.1](https://www.amazon.de/dp/B07RXSKPBX)
* [T-Beam V1.0](https://www.amazon.de/dp/B07RT9FKPL)

Bu kartlar yaklaşık 20 Euro tutarında, çok ucuz ve LoRa iGate için mükemmel. Unutmayın: 433MHz sürümüne ihtiyacınız var!

## Derleme ve Yapılandırma

**Almanca bir [hızlı başlangıç ](https://www.lora-aprs.info/docs/LoRa_APRS_iGate/quick-start-guide/) sayfası var! Bir göz atın;)**

**Fransızca bir [hızlı başlangıç](http://www.f5kmy.fr/spip.php?article509) sayfası var! Bir göz atın ;)**

### Nasıl derlenir

En iyi başarıyı PlatformIO kullanarak elde edersiniz (ve size destek olabileceğim tek platform budur).

* [PlatformIO](https://platformio.org/) gidin, IDE'yi indirin ve kurun.
* Kurulduysa IDE'yi açın, soldaki tarafta 'uzantılar' a tıklayın, ardından 'PlatformIO' arayın ve kurulumu yapın.
* Kurulduğunda sol taraftaki 'karınca başı' na tıklayın ve sağ tarafta projeyi içe aktarmayı seçin.
* Sadece klasörü açın ve Yazılımı derleyebilirsiniz.
  
### Yapılandırma

* Tüm yapılandırma değişiklikleri için gerekli ayarları **data/is-cfg.json** dosyasında bulabilirsiniz.
* Kartınıza yüklemek için bunu PlatformIO üzerinden **Upload File System image** şeklinde yapmanız gerekmektedir!
* **Upload File System image** bulmak için PlatformIO simgesine (küçük uzaylı) tıklayın, yapılandırmanızı seçin, 'Platform' u tıklayın ve **Upload File System image** yi arayın.


## Bu depoda dallar ve sürüm sistemi

Bu yazılım, sürekli sürüm yayını sisteminde geliştirilmektedir: her gün yeni bir sürüm oluşturulabilir. Ancak, yeni pull isteklerinin nereye gideceği ve sürüm sisteminin nasıl görüneceği konusunda hala kurallar vardır.

### Sürüm sistemi

Eğer develop dalı yeterince kararlıysa, yeni bir sürüm için birleştirilir ve master dala bir pull isteği ile birleştirilir ve yeni bir sürüm oluşturulur.

Sürümler şu ayarlara dayanmaktadır:
* büyük: geçerli yıl (2 haneli)
* küçük: yılın geçerli haftası
* yama: önemli bir düzeltme varsa, sadece numarayı artırın, aksi takdirde 0

*örnek: 11/14/2020 tarihinde yeni bir sürüm oluşturulursa, bu sürüm numaraları kullanılacaktır:
* büyük: 20
* küçük: 46
* yama: 0

bu yüzden sürüm şu şekilde olacaktır: 20.46.0

## Gelecek Planlar

* [x] Sonraki yayına kadar zamanı göster
* [x] IS sunucusundan giriş sorunlarını göster
* [ ] Çeşitli farklı OLED'leri desteklemek için daha iyi bir OLED kütüphanesi ekleyin
* [ ] Sıcaklık çipleri (BMExxx) için destek ekleyin
* [x] Yapılandırmayı yüklemek için FTP sunucusu desteği ekleyin
* [ ] Yapılandırma ve diğer şeyler için web sunucusu ekleyin
* [ ] Alınan paketler için istatistikler ekleyin
* [ ] Harita üzerinde alınan paketleri gösterin
* [ ] vb.

## LoRa Tracker

Diğer projeme bakın: a [LoRa Tracker](https://github.com/peterus/LoRa_APRS_Tracker)

## İpuçları

### HFarklı kartların bazı özellikleri şunlardır

* TTGO T-Beam V1.0 ve V1.1 ve SSD1306 OLED ekranı

SSD1306 0,96" OLED ekranını doğrudan kart üzerine eklerken dikkatli olmanız gerekir, çünkü piyasada iki farklı pinout versiyonu vardır.
Doğrudan montaj için, bu Pinout'a sahip bir ekran gerekir -> [VCC - GND - SCL - SDA](pics/display-right.jpg).
Diğer ekranın [doğrudan montajı](pics/display-wrong.jpg) teller olmadan mümkün değildir!
'Wrong' ekran da çalışır ancak VCC ve GND'yi tel ile değiştirmeniz gerekir!

[LoRa APRS WiKi Displays](https://github.com/lora-aprs/LoRa_APRS_Tracker/wiki/Displays) sayfasında daha fazla ayrıntı bulunmaktadır.

İpuçları eklemekten çekinmeyin!
