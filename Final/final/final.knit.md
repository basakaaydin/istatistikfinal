---
title: "Yıllık Gelirdeki Farklılıklara Sebep Olan Faktörler"
author: 
  - Başak Aydın[^1]
bibliography: ../bibliography/biblio.bib
csl: ../csl/apa-tr.csl
header-includes:
  - \usepackage{polyglossia}
  - \setmainlanguage{turkish}
  - \usepackage{booktabs}
  - \usepackage{caption} 
  - \captionsetup[table]{skip=10pt}
output:
  bookdown::pdf_document2:
    fig_caption: yes
    fig_height: 3
    fig_width: 4
    keep_tex: no
    latex_engine: xelatex
    number_sections: yes
    toc: no
geometry: margin=1in
link-citations: yes
urlcolor: blue
fontsize: 12pt
biblio-style: apalike
abstract: |
  Bu bölümde çalışmanızın özetini yazınız.
---


<!-- ======================================================================= -->
<!-- ============================== NOTLAR ================================= -->
<!-- ======================================================================= -->
[^1]: 21080560, [Github Repo](https://github.com/basakaaydin/istatistikfinal)




# Giriş
 Yapmış olduğum bu çalışmada araştırma sorum yıllık gelirdeki değişimleri etkileyen faktörler nelerdir sorusuna dayanmaktadır.Bu sorudan yola çıkarak elde ettiğim sonuçların gelir üzerindeki etkisini incelemek ve veriyi analiz etmek projemin konusunu oluşturmaktadır.Araştırmama dair kullandığım veri setini UCI Machine Learning Repository sitesi üzerinden aldım.Bu veri seti nüfus sayımı verilerine dayanarak yıllık gelirin 50.000$'ı aşıp aşmadığını incelemektedir.Veri setim toplam 14 değişken ve 48.842 gözlem içermektedir.Değişkenler age,workclass,fnlwgt,education,education-num,marital-status,occupation,relationship,race,sex,capital gain,capital loss,hours per week,native country'den oluşmaktadır. 


## Çalışmanın Amacı
Bu araştırmada yaş,etnik grup,cinsiyet,eğitim,medeni hali gibi değişkenlerine göre gelirin farklılık gösterip göstermediği incelenmiştir.
 
 Birçok ülke,kurum ve kuruluşlar iş dünyasında ayrım yapmaksızın fırsat eşitliğine yönelik çeşitli hükümlerde bulunsa da iş hayatında dolayısıyla ücretlerde çok bariz farklılıklar bulunmaktadır.
 
 Bu farklılıkların hangi değişkenlerden kaynaklandığını tespit ederek,yorumlayıp,bir bakış açısı oluşturup,çözümler sunabilmek bu çalışmanın amacıdır.


## Literatür 

 İş gücü piyasasında cinsiyet,etnik köken,ırk,yaş,din gibi birçok faktörlerden kaynaklanan ayrımcılığın ABD,Çin,Güney Kore ve bunun gibi birçok güçlü devletlerde bariz bir sorun olduğunu görüyoruz.Ayrımcılık özellikle iş ortamında ücret,iş alma ve terfi konularında yoğunlaşıyor.Bu tarz ayrımcılıklar işgücü piyasalarının gelişimini ve işleyişini aynı zamanda geliri etkileyen en temel sorunlardan birisidir.Kişisel ücret farklılıklarında aynı birimde çalışan işçilerin yaş ve cinsiyetine göre çok büyük faklılıkların olduğu bariz.Eşit işe eşit ücret sağlanması gerektiği halde bu göz ardı ediliyor.Bunun en iyi örneği kadın işçiye aynı işi yapması için erkek işçiden daha az ücret ödenmesi durumudur.Toplumsal cinsiyet eşitsizliği ya da bir başka deyişle cinsiyete dayalı işbölümü temelinde kadınlar erkekler ile aynı eğitim düzeyine ve mesleki kıdeme sahip olsalar bile sadece kadın olmalarından kaynaklı cinsiyetçi ücret ayrımına maruz kalmaktadır.Bunu yıllık gelire vurduğumuzda kadınlardaki yıllık gelir erkeklerdekine göre daha düşük bir meblağ olarak istatistiklere yansıyor. @seher2016icsgucu
 
 İş gücü piyasasında cinsiyet dışında medeni durum,yaş,eğitim düzeyi,mesleki tecrübe ve verimlilik gibi iş gücünün özelliğinden kaynaklanan ücret/gelir farklılıkları da bulunmaktadır.Sektör özellikleri ve bölgeler arası ücret farklılıklarından kaynaklanan yıllık gelir farklılıkları da bulunmaktadır.İşgücü piyasalarında işleri ve ücretleri farklılaştıran bir başka unsur da firma ölçeğidir. Hemen her yerde ve zamanda gözlenen bir durum büyük firmalarda ücretlerin küçük firmalara oranla daha yüksek olmasıdır. Büyük firmalarda ücretlerin yüksek olması işleri birbirinden heterojen kılarak ücretlerin farklılaşmasına yol açar.  @maktav2019icsgucu
 
 Etkin Ücret Teorisine göre işçiyi denetlemenin ve performansını ölçmenin zor olduğu, işçinin hatalı üretim yapmasının maliyetli olduğu, işin belirli bir süre spesifik işyerinde eğitim gerektirdiği durumlarda işverenlerin istekli olarak piyasa denge ücretinin üstünde ücret (etkin ücret ödemesi) verdikleri söylenebilir. Etkin ücret ödemelerinin işleri birbirinden farklı (heterojen) hale getirerek emek piyasalarında ücret farklılıklarına neden olabileceğini belirtmek gerekir. Benzeri özelliklere sahip iki işçiden birisi etkin ücret uygulamasının yapıldığı firma veya işkolunda çalışıyorsa diğerinden daha yüksek ücret alabilmektedir. @blackaby1991industry
 Bir diğer gelirdeki farklılıkların nedeni ise ırktır.Siyah ve beyaz ayrımı geçmişten bugüne devam eden bir sorundur.Siyah erkeklerin hala birçok işyerinde aynı meslekte çalışan beyaz erkeklerden daha düşük bir ücret aldığını istatistikler birçok kez göstermiştir.Bunun yanı sıra gelirdeki farklılıklar ırksal eğitim eşitsizliği ile de doğru orantılı.Örneğin ABD'deki istatistiklere göre beyaz ailelerin %39'u lisans eğitimi veya yüksek eğitim mezunu iken siyahi ve hispanik ailelerde bu oran %23 ve %17'dir.Irklar arasındaki eğitim durumu farkı iş hayatında daha az ücretle çalışma ya da tercih edilmeme gibi durumlara yol açıyor. @stolzenberg1975education
 
 Sonuç olarak iş gücü piyasasında karşılaştığımız birçok değişken faktör gelirdeki farklılıkların neyden,hangi değişkenlerden kaynaklandığını anlamamıza ve analiz etmemize yardımcı olmaktadır.


# Veri 
Bu bölümde çalışmanızda kullandığınız veri setinin kaynağını, ham veri üzerinde herhangi bir işlem yaptıysanız bu işlemleri ve veri seti ile ilgili özet istatistikleri tartışınız. Bu bölümde tüm değişkenlere ait özet istatistikleri (ortalama, standart sapma, minimum, maksimum, vb. değerleri) içeren bir tablo (Tablo \ref{tab:ozet}) olması zorunludur. Tablolarınıza gerekli göndermeleri bir önceki cümlede gösterildiği gibi yapınız. [@perkins:1991]

Analize ait R kodları bu bölümde başlamalıdır. Bu bölümde veri setini R'a aktaran ve özet istatistikleri üreten kodlar yer almalıdır.


```r
library(tidyverse)
library(here)
adult_data <- read_csv(here("C:/Users/basak/OneDrive/Masaüstü/istatistikfinal/Final/data/AnyConv.com__adult.data - Kopya (2).csv"))
```

 





\begin{table}[ht]
\centering
\caption{Özet İstatistikler} 
\label{tab:ozet}
\begin{tabular}{lccccc}
  \toprule
 & Ortalama & Std.Sap & Min & Medyan & Mak \\ 
  \midrule
capital gain & 7663.83 & 422.97 & 1055.00 & 7688.00 & 15024.00 \\ 
  hours per week & 40.44 & 12.35 & 1.00 & 40.00 & 99.00 \\ 
  yearly income & 43024.94 & 700.03 & 37000.00 & 43000.00 & 70000.00 \\ 
   \bottomrule
\end{tabular}
\end{table}


# Yöntem ve Veri Analizi
Bu bölümde veri setindeki bilgileri kullanarak çalışmanın amacına ulaşmak için kullanılacak yöntemleri açıklayın. Derste işlenen/işlenecek olan analiz yöntemlerinden (Hipotez testleri ve korelasyon analizi gibi) çalışmanın amacına ve veri setine uygun olanlar bu bölümde kullanılmalıdır. [@newbold:2003; @ozsoy:2010; @ozsoy:2014]

Örneğin, regresyon analizi gerçekleştiriyorsanız tahmin ettiğiniz denklemi bu bölümde tartışınız. Denklemlerinizi ve matematiksel ifadeleri $LaTeX$ kullanarak yazınız.

$$
Y_t = \beta_0 + \beta_N N_t + \beta_P P_t + \beta_I I_t + \varepsilon_t
$$

Bu bölümde analize ilişkin farklı tablolar ve grafiklere yer verilmelidir. Çalışmanıza uygun biçimde histogram, nokta grafiği (Şekil \@ref(fig:plot) gibi), kutu grafiği, vb. grafikleri bu bölüme ekleyiniz. Şekillerinize de gerekli göndermeleri bir önceki cümlede gösterildiği gibi yapınız.



```r
adult_data %>% 
  ggplot(aes(x = Age, y = `yearly income`)) +
  geom_point() +
  geom_smooth() +
  scale_x_continuous("age") + 
  scale_y_continuous("yearly income")
```

\begin{figure}

{\centering \includegraphics{final_files/figure-latex/plot-1} 

}

\caption{Yıllık Gelir Farklılıkları}(\#fig:plot)
\end{figure}


# Sonuç
Bu bölümde çalışmanızın sonuçlarını özetleyiniz. Sonuçlarınızın başlangıçta belirlediğiniz araştırma sorusuna ne derece cevap verdiğini ve ileride bu çalışmanın nasıl geliştirilebileceğini tartışınız.

**Kaynakça bölümü Rmarkdown tarafından otomatik olarak oluşturulmaktadır. Taslak dosyada Kaynakça kısmında herhangi bir değişikliğe gerek yoktur.** 

**_Taslakta bu cümleden sonra yer alan hiçbir şey silinmemelidir._**

\newpage
# Kaynakça {#references}
<div id="refs"></div>

