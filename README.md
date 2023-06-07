# OTOBÜS BİLETİ SATIŞ UYGULAMASI
Yapacağım uygulama otobüs şirketlerinde bilet satışını takip etmede kullanılacaktır.
## UYGULAMANIN İÇERİĞİ
Uygulamada bir yolcu gideceği yeri seçtikten sonra aktif otobüs firmaları listenecektir.Sayfanın sol kısmında seçilen otobüsün koltukları yer alacaktır.İstenilen bilgileri doldurup bileti alacaktır.Müşteri bu uygulamada otobüs firmalarındaki indirimleri, istediği firma ve koltuğu seçebilecektir. Koltuk seçiminde güneşin hangi yönden vuracağını görebilecektir.Bileti alınca firmalara göre kuponlar,mağazalarda geçerli indirimler verilecektir.Özel günlerde biletlerde indirimlerden yararlanabilecektirler.Güzergah hakkında bilgilendirmeye sahip bir uygulamadır. Mola yerlerini ve saatlerini bileceklerdir.En önemlisi bazı otobüs firmalarında sabah seferlerinde ikramlıklar farklılık gösterebilir. Otobüslerde internet ve prizlerin var olup olmadığını görebileciktirler.Sefer hakkında bilgi almak için yorum kısmına istediğini yazabilirler.
## UYGULAMA YAPIM AŞAMASI
Uygulama Windows Forms ile yapılacaktır.
## UYGULAMA YAPIM ADIMLARI
Öncelikle Windows Forms dosyası açalım. Ardından yapacağımız uygulamayı adım adım planlayalım.Yani ilk ne yapacağız sonra ne ile devam edeceğiz gibi.
  * En üstte otobüs seçim kutucuğu olacak firma adları listelenecektir.
  * İstikamet adı altında kalkış ve varış yerleri seçilecektir.
  * Tarih kutucuğu ve fiyat kutucuğu ile o kısmı bitirmiş olacağız.
  * Yukarıdaki işaretlemeler bittikten sonra sol tarafta seçtiğimiz otobüs firmasının koltukları belirecektir. Oradan farede sağ tık ile rezerve et seçeneği ile koltuğu satın almak için bir diğer işleme geçilecektir.Yeni bir form oluşturup orada müşteri adı,soyadı ve cinsiyeti işaretlenip kayıt edilecektir. Koltuk satıldığında kadın ise kırmızı erkek ise mavi olarak boyanacaktır.

Yukarıda verdiğim adımları sırasıyla yapmaya başlayabiliriz.Araç kutusundan label seçip 5 tane label ekleyelim formumuza.3 tane ComboBox, 1 tane DateTimePicker,1 tane buton ve NumericUpDown araçlarını ekleyelim.Bu eklediklerimizi düzenleyip formda yerlerine koyalım.
  
![giris1](https://github.com/dilankln/biletsatis.io/assets/102542430/c6ffa302-9f5b-4ff5-bc84-4ebe3c658d47)

+ label1=Otobüs seçiniz:
+ label2=Kalkış Yeri:
+ label3=Varış Yeri:
+ label4=Tarih:
+ label5=Fiyat:

Kalkış yeri ve varış yerini groupbox içerisine alıp ismini istikamet yapalım.
Nasıl değiştirdiğimizi bir tanesinde sizlere göstereceğim diğerlerine de aynı işlemi uygulayacağız.

![ornek1](https://github.com/dilankln/biletsatis.io/assets/102542430/df1714c0-ffb5-4d1e-bc7a-86b05ccefb0e)

Özellikler kısmında Text yazan yere istediğimizi yazıyoruz.Yazı boyutu,renki  ve şekli için oradaki Font kısmına tıklayıp ayarlayabilirsiniz.
Şimdi diğer labelleri değiştirip son halini sizlere göstereceğim.

![giris2](https://github.com/dilankln/biletsatis.io/assets/102542430/c6ae5c4e-9557-45ea-86a6-9fb9f6295a31)

Yaptığımız işlemlerden sonraki hali bu.Şimdi kod kısmında bizlere kolaylık olması adına labeller hariç eklediğimiz diğer araçların isimlerini kısaltalım. Yine bir örnek vereceğim aynı şekilde diğerlerine de uygulayın.

![giris3](https://github.com/dilankln/biletsatis.io/assets/102542430/3c910b6f-13fe-4409-9372-7dc581649ed1)

Diğerlerini ne adla kısalttığımı yazacağım sonrasında ise yeni form oluşturacağız.
+ ComboBox2= cmbNereden
+ ComboBox3= cmbNereye
+ DateTimePicker= dtpTarih
+ NumericUpDown=nudFiyat

Şeklinde kısalttım.
