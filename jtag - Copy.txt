jtag hata ayıklama, pcb deki bağlantıları test etmeye yarar (boundary scanning)
bsdl (boundary scan description language) : Sınır tarama açıklama dili, JTAG kullanarak elektronik test için bir donanım açıklama dilidir.

sayısal devrelerin jtag arabirimi ile test edilmesi sürecinde kullanılan bir hardware description language*. vhdl'in alt kümesi gibi düşünülebili



JTAG (Joint Test Action Group) veya sınır taraması, IEEE 1149.1 standardıdır.

TAG 1990'dan beri gelişti ve şimdi sistem içi programlama, sınır tarama testi ve yazılım hata ayıklama ve öykünme için kullanılabilir.

Çip üreticileri, geliştiricilere JTAG arayüzü üzerinden mikrodenetleyici ile bağlantı kurma yeteneği vermek için standartta tanımlanan Test Erişim Bağlantı Noktasını (TAP) uygular. Mikrodenetleyiciniz üzerindeki 4 veya 5 pinden oluşur – TDI, TDO, TMS, TCK ve isteğe bağlı bir TRST.

 Son 30 yılda standart, otomatik test geliştirme ve karışık sinyal testi için BSDL (Sınır-Tarama Tanımlama Dili) ile genişletildi.

 Kartınızda yeniden programlamak, hata ayıklamak veya sınır tarama testi yapmak istediğinizde, makinenizden JTAG hatları üzerinden veri gönderebilirsiniz. 

TDI -> Test data input
TDO -> Test data output
TMS -> Test mode select
TCK -> Test clock input


 Sınır tarama bileşenlerinin ve gelişmiş sınır tarama araçlarının artan sayısı ve ayrıca daha sonra açıklanacak olan diğer faktörler, mühendislere aşağıdaki faydaları sağlar:

Test Edilebilirlik İçin Tasarım (DFT) kurallarını uygulamak kolaydır. Bu makalenin ilerleyen bölümlerinde temel DFT kurallarının bir listesi sağlanmaktadır.

Test edilebilirliği artırmak için PCB yerleşiminden önce tasarım analizi.

Paketleme sorunları PCB yerleşiminden önce bulunur.

Test noktalarına çok az ihtiyaç vardır.

Test fikstürlerine gerek yok.

Test süreci üzerinde daha fazla kontrol.

Herhangi bir fonksiyonel test kodu yazmadan ara bağlantı problemlerinin hızlı teşhisi (yüksek çözünürlüklü).

Flash cihazlarda program kodu.

CPLD'lere konfigürasyon verisi yerleşimi tasarlayın.

JTAG öykünmesi ve kaynak düzeyinde hata ayıklama.


Sınır tarama tekniği, yeni paketleme teknolojileri nedeniyle gittikçe komplike hale gelen baskılı devre kartlarının üzerindeki fiziksel erişim problemlerini çözebilmek için 1980'lerin sonlarında geliştirilen bir test tekniğidir. Sınır tarama tekniği, aynı zamanda entegre devrelerin pin durumlarını izlemede, voltajlarını ölçmede, ya da entegre devrelerin alt bloklarını analiz etmede düzeltme tekniği olarak da kullanılır.


1990 yılında JTAG (Joint Test Action Group) tarafından BGA kılıf tipindeki malzemelerin kontrol ve
testini mümkün kılacak ‘BOUNDARY SCAN TEST’ (BS)
standardı geliştirildi. IEEE Std. 1149.1 standardı olarak kabul edildi. Bu standarda bazı kayaklarda JTAG
da denilir.

Şekil 3.2.’de görüldüğü gibi, IC devre içerisinde iken
(in-circuit test) yaklaşık 5 adet bağlantı yapılarak BS
testi yapmak mümkündür. Bu bacak isimleri; TDI,
TDO, TMS, TCK ve TRST ’dir. IC deki bu bacaklar
sadece BS testi işlemine ayrılmıştır. 


BS testi ile yapılan testler şunlardır;
sistem erişim testi, BS test erişimi, hafıza testi, flash
programlama, FPGA / CPLD programlama, CPU emulatörü, entegrenin sağlamlığı, bacaklarındaki lehim
temas durumu, malzeme bacaklarındaki açık veya
kısa devre bağlantılar. 


 Buradaki register yapılar bu işlemlere yardımcı
olmaktadır. ‘Bypass register’ başka bir IC verisi gönderilirken, çakışma olmamasını sağlar. ‘Device Identification Register’ veya kısaca ‘Device ID’ test edilen
malzemenin tanımlanmasını sağlar. TAP test edilecek
malzemenin doğru şekilde seçilmesine yardımcı olur. 



veri yolu üzerinde kullanılan entegreler (IC)


