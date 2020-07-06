# iv-hafta-odevi
*  Geri dönen bilgiye göre yeşil renkte onay mesajı gösterilmesi. (örneğin:view bag)

*  AddMVC - AddMVCCore - AddDateAnnotations nedir? Nerelerde eklenmelidir?

 * Shanpshot nedir? nasıl değişir? neden alınır?

*  Jquery Calender--> [Datapicker](https://jqueryui.com/datepicker/) --> DueAt'i takvim tipinde eklemek nasıl yapılır? Araştırınız. (DateTimeUffset tipinden atamalar oluşucak)

*  First- FirstOrDefault ve Single- SingleOrDefault nedir? Aralarındaki farkı araştırınız.

*  En kısa null check nasıl yapılır?

* partial view nedir?

* Farklı authentication bulup,aynı işleri farklı yollar ile yapanları araştırınız.

* Ödev- Razor Pages/MVC Projects karşılaştırmasını yapınız.



**AddMvc() , AddMvcCore() , AddDateAnnotations nedir?**


Startup sınıfının ConfigureServices () öğesinde bu iki yöntem (AddMvc () ve AddMvcCore ()) kullanılmaktadır .ConfigureServices () yöntemine gidildiğinde IServiceCollection - AddMvc () ve AddMvcCore () 'de iki yöntem bulacaksınız. Aşağıdaki şekilde, Visual Studio düzenleyicisinde gösterilmektedir.


![T_AddMvcAddMvcCore_01](https://user-images.githubusercontent.com/66273342/86607462-f04e4780-bfb1-11ea-9e72-34cd894258e3.png)


AddMvcCore () yöntemi aşağıda gösterilmiştir;


![AddMVCCore](https://user-images.githubusercontent.com/66273342/86607526-06f49e80-bfb2-11ea-8d30-3cb7d72d45ec.png)


AddMvc () kaynak kodunun parçası aşağıda verilmiştir;


![AddMVC](https://user-images.githubusercontent.com/66273342/86607496-fe03cd00-bfb1-11ea-955f-12c06db5629d.png)


**Data Annotations Nedir?**

MVC uygulamasında veri tabanı tablolarını Code First yöntemi ile oluşturmaya başladığımızda yapılan validasyon işlemlerine Data Annotations denir.



Shanpshot nedir? nasıl değişir? neden alınır?

Snapshot’ı kısa süreli çalışmalar öncesinde backup almak yerine snapshot’ı kullanabiliriz. Snapshot sayesinde sanal makinamızın anlık ekran görüntüsü alınır ve siz herhangi bir sebepten dolayı sanal makina üzerinde yaptığınız işlemleri geri almak istediğinizde almış olduğunuz snapshot’a revert diyerek eski haline geri dönüş yapabilirsiniz.Snapshot kısa süreli işlemler için kullanılması tavsiye ediliyor. Örneğin bir update yapacaksınız ve update 1 veya 2 hafta sürecek. Bu durumda snapshot almak çok doğru değil. Böyle bir operasyonda backup  veya clone alarak daha rahat birşekilde işlemlerinize devam edilebilir.


First- FirstOrDefault ve Single- SingleOrDefault nedir? Aralarındaki farkı araştırınız.--> https://medium.com/@ruveydakardelcetin/single-singleordefault-ve-first-firstordefault-fark%C4%B1-d7657eec8d02



En kısa null check nasıl yapılır?

Belirtilen dizenin null mi yoksa boş bir dize mi ("") olduğunu gösterir.--> public static bool IsNullOrEmpty (string value);


Aşağıdaki örnek üç dizeyi inceler ve her bir dizenin bir değere sahip olup olmadığını, boş bir dize mi olduğunu veya nullolduğunu belirler.

![null](https://user-images.githubusercontent.com/66273342/86617141-7fae2780-bfbf-11ea-9364-946cfe29f728.PNG)



Partial view nedir?


Bir işlemi birden fazla kez yapacaksak bir kalıp kullanırız. Örnğin oluşturacağımız bir resim galerisini web sitesinde birden fazla sayfada kullanacağımızı düşünelim. Aynı galeriyi her sayfa için tekrar tekrar oluşturmak gereksiz ve zaman kaybıdır. Tam da burada Partial View  imdadımıza yetişiyor. Partial View kendi başına hiçbir işlevi olmayan bir yapıdır. Bulunduğu sayfa içerisinde çalışır.Kısacası; tkrar etmemiz gereken nesneleri, html sayfalarını rahatlıktla bu şekilde kullanabiliriz.


**API’larda İstemci Doğrulama Yöntemleri (API Authentication Ways);**

Doğrulama organizasyonların ağlarını güvenli bir şekilde sadece izin verilen kullanıcılar veya işlemler tarafından erişilebilir ve tüketilebilir olmasını sağlar.

1. Bilgi Faktörü (Knowledge Factor):Bu faktörde kullanıcıya ait bilgilere erişirken genellikle bir kullanıcı adı veya email kullanılır ve bu şekilde kullanıcının bildiği şeye erişim sağlanır.

2. Mülk Faktörü (Possession Factor):Örneğin güvenli bir anahtar taşıyan flash bellek, bir telefon veya farklı bir donanım ile sağlanan bilgilerdir.

3. Varlık Faktörü (Inherence Factor):Basitçe ayırt edici bilginin vucudunuzda olduğu senaryodur.

4. Konum Faktörü (Location Factor):Örneğin bir bankacılık sisteminde son yaptığınız işlem Manisa’da bir POS cihazı iken 10 dakika sonra kartınızın İstanbul’da kullanılması ile bankaların bu doğrulama yöntemi ile kredi/banka kartlarının kayıp/çalıntı gibi işlemlerini takip etmektedir.

5. Zaman Faktörü (Time Factor):Erişilmek istenilen kaynağın erişilemez olduğu zamanlarda yapılan erişim isteklerinin kaydedildiği ve konum faktörüyle kombine edilerek kullanıcının doğrulandığı ya da tehdit olarak algılandığı bilgilerdir.

6. Davranış Faktörü (Gesture Factor):Örneğin resim şifre denen kullanıcının ilgili resim üzerinde yaptığı jestler ve dokunuşların kaydedildiği ve bu şekilde doğrulandığı sistemler verilebilir.

7. Tek Faktörlü Doğrulama:Doğrulama yöntemlerinden sadece bir tanesinin kullanılarak doğrulama işleminin gerçekleştirilmesidir.

8. İki Faktörlü Doğrulama:İki doğrulama faktörünün birbirini tamamlayıcı olarak veya doğrulamanın çok mühim olduğu ortamlarda çaprazlama yapmak amaçlı kullanıldığı yöntemdir.

9. Çok Faktörlü Doğrulama:En olağan dışı, paranoyakça ve yorucu olan yöntem ise Multi-Factor dediğimiz çok aşamalı yöntemlerle sistemlerin kullanıcılarını doğrulamasıdır.



**Razor Pages/MVC Projects karşılaştırmasını yapınız.**

Razor View ve WebForms gibi dosyanın arkasında kodlar mevcut olmasına rağmen, MVC ise kontrolör, görünüm ve model için farklı dizinlerde ayrı dosyalara sahiptir.Aşağıdaki görselde görünüm olarak farkları mevcuttur.


![mvc vs razor](https://user-images.githubusercontent.com/66273342/86614305-76bb5700-bfbb-11ea-9bf9-a469173cba4e.png)


Bir HTTP POST için MVC'de, nesnemizi MVC eylemine iletiriz (örn. “ManagePage (int id, PageClass sayfası)”). Razor Page ile bunun yerine iki yönlü veri bağlama özelliğini kullanabiliriz.Razor Pages uygulamasının gerçek sayfalar olması ve tüm AJAX / REST API işlevlerinin MVC ile uygulanması fikri her zaman kullanışlıdır.MVC'nin süper esnek olması ise kullanılabilir olmasında etkendir, ancak bunu daha karmaşık hale getiren de budur. Razor Pages'ın en önemli özelliği ise sadeliğidir.


