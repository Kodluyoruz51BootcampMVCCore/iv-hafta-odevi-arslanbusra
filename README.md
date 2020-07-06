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


Parial view nedir?


Bir işlemi birden fazla kez yapacaksak bir kalıp kullanırız. Örnğin oluşturacağımız bir resim galerisini web sitesinde birden fazla sayfada kullanacağımızı düşünelim. Aynı galeriyi her sayfa için tekrar tekrar oluşturmak gereksiz ve zaman kaybıdır. Tam da burada Partial View  imdadımıza yetişiyor. Partial View kendi başına hiçbir işlevi olmayan bir yapıdır. Bulunduğu sayfa içerisinde çalışır.Kısacası; tkrar etmemiz gereken nesneleri, html sayfalarını rahatlıktla bu şekilde kullanabiliriz.


