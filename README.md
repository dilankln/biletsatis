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

  
![giris](https://github.com/dilankln/biletsatis.io/assets/102542430/d3061ad6-0660-4af5-9f8b-45fd5a2a4c0d)
