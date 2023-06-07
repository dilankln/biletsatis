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
Yeni öge ekle seçeneğine tıklayıp Formu seçelim ismini KayıtFormu yapalım.

![giris4](https://github.com/dilankln/biletsatis.io/assets/102542430/7a60f2b8-6229-4634-826c-98ccf9a06cbd)

Eğer yeni öge ekle seçeneğini bulamadıysanız arama kutucuğuna yazarak da ulaşabilirsiniz.
Yeni oluşturduğumuz forma ise 2 tane label, 2 tane textBox kutucuğu,2 tane radioButton ve 2 tane buton ekleyip yerlerine yerleştirelim.

![kayıt](https://github.com/dilankln/biletsatis.io/assets/102542430/49f978e1-53e1-4614-970a-7b3b8b304aed)

+ label1=İsim:
+ label2=Soyisim:
+ radioButton1=Bay
+ radioButton2=Bayan
+ button1=İptal
+ button2=Tamam

şeklinde düzenleyelim ve nasıl göründüğüne bakalım.

![kayıt2](https://github.com/dilankln/biletsatis.io/assets/102542430/030ce7ad-e18c-44ab-ab99-f7f9f027cf7c)

Bir önceki formda yaptığımız gibi yine kısaltma işlemi yapalım.
 + textBox1=txtIsim
 + textBox2=txtSoyisim
 + radioButton1=rdbBay
 + radioButton2=rdbBayan
 + button1=btnIptal
 + button2=btnTamam

şeklinde kısaltmalarımızı yapıp işimizi kolaylaştıralım.
İlk yaptığımız forma gelip otobüs seçin yazdığımız comboBoxa çif tıklayıp otobüs firmalarımızı oluşturalım koltuklarıyla beraber.
Sizlere ilk görselini gösterip ardından anlatımını yapacağım. Anlatımı basit ve kısa tutacağım en anlaşılır halde olmasını sağlayacağım.

![otobus](https://github.com/dilankln/biletsatis.io/assets/102542430/ba47a7fd-a993-45a8-ae90-6430b29e9f03)

Switch-case yöntemi ile seçim yapılmasını sağladık.Burada KoltukDoldur() fonksiyonunu oluşturdum bu kısım bittikten sonra oluşturduğum fonksiyonu da anlatacağım.Oluşturduğum fonksiyonun parantez içindeki sayılar otobüsteki arka arkaya kaç koltuk yani kaç sıra olduğunu belirler.3 tane otobüs firması oluşturdum vee hepsinin koltuklarını farklı sayıda yaptım. Koltukların görünümünü sizlere göstermeden öne koltukları 2-2 ayıralım ve arkadaki beşli koltuğu düzenleyelim.

![koltuk](https://github.com/dilankln/biletsatis.io/assets/102542430/d2330e32-e949-4e2d-9afb-694149a73254)

Burada koltuk numaralarını for döngüsü ile sıraladım.Sadece beşli koltuk bölünmeyecek şekilde kodları yazdım.Koltukların görünümünü height ve width ile ayarladım.Koltuk_MouseDown adında oluşturduğum yeni fonksiyon ile rezerve etme işlemini kolaylaştıracağız tabii biraz daha ilerde anlatacağım o kısmı.Koltukların bu üç firmadaki görünümlerine bakalım.

![selcuk](https://github.com/dilankln/biletsatis.io/assets/102542430/0cb19ca5-c14a-4d9a-8581-3cd788425d1d)
Selçuk Truzim

![zafer](https://github.com/dilankln/biletsatis.io/assets/102542430/e985ec9b-07c7-43b6-a70f-d909d7002231)
Zafer Truzim

![kılın](https://github.com/dilankln/biletsatis.io/assets/102542430/520cd53e-4b26-4b53-90f4-8e8611f23d9b)
Kılın Truzim 
