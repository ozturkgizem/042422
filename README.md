# 17.06.2022

YILDIZ TEKNİK ÜNİVERSİTESİ
KİMYA-METALURJİ FAKÜLTESİ
MATEMATİK MÜHENDİSLİĞİ 

*Matematik Mühendisliği Bitirme Projesi*

***BUZULLAR ÜZERİNE VERİ BİLİMİ ve İLİŞKİLENDİRME ÇALIŞMASI***

*Proje Danışmanı: Dr. Öğretim Üyesi Nilgün Güler Bayazıt*
*18052054 Öztürk, Gizem*

*Buzullar, okyanus yaşamı, iklim döngüsü, su döngüsü, deniz yüksekliği, okyanus sıcaklığı, nem akışı, rüzgarlar gibi pek çok parametreden etkilendiği ve aynı zamanda bu parametreleri etkilemesi nedeniyle ilgi çekici bir araştırma konusudur. Buzulların erimesindeki artış, buz kütlelerin yerleşik buzlardan kopması, erime ve donma zamanlarındaki değişim ve su yollarının değişmesi küresel iklim ve ticaret yolları açısından önem arz etmektedir.*

## İçerik

Bu çalışmada buzulların okyanusa, atmosfer ve matematikle yakın ilişkisi göz önüne alınarak deniz buzu konsantrasyonu (SIC) ve alanı (SIE) üzerine bir derin öğrenme modeli eğitilmiştir. Buzulların genişliği ve konsantrasyonu etkileyen parametrelere ve kullanılan modellere dair geniş bir görüş açısı kazanabilmek adına oldukça detaylı bir literatür çalışması yapılmıştır. 

* Bu çalışma için geliştirilen modelde basit bir doğrusal regresyon iskeleti, trendi giderilmiş ızgaralanmış veriler ve basit bir korelasyon/ağırlıklandırma şeması kullanmıştır. 

* Model girdi olarak ızgaralanmış buz konsantrasyonu verisi ve deniz buzu indeksi verilerini alır. Veri önişleme olarak deniz buzu konsantrasyonu verileri ızgaralanır ve kaydedilir. 

* Izgaralanan Deniz Buzu Konsantrasyonu verileri görselleştirilmiş ve tahmin verileri grafikleştirilmiştir. 

* Kullanılan veri setleri NASA/ NSIDC tarafından sağlanan deniz buzu konsantrasyonu ve deniz buzu indeksi veri setleridir. Proje dosyası, kullanılan veri setini, ızgaralanmış Arctic ve Antarktik verilerini, tahmin fonksiyonları ve dosyalarını, grafikleri ve figürleri içerir.

## Araştırmanın Çerçevesi

Çalışmada Arktik buzul bölgesi odaklı mevsimsel tahminlere odaklanılmıştır ve Antarktika buzul bölgesi için de tahmin üretebilme yetisindedir. Model, deniz buzu durumunun ızgaralı uzamsal verilerini kullanarak herhangi bir ay veya yıl için (1980'den beri) aylık ortalama deniz buzu alanını veya kapsamını tahmin edebilir. 

İlk aşamada Arctik ve Antartika deniz buzu konsantrasyonu verilerine NASA Earth Data platformu ile erişilmiştir. Daha sonra bu veriler ızgarlanıp kaydedilmiştir. 

```diff
+ 2016’ya kadar olan verilen kaynak olarak kullanılan projeden, 
+ 2016 sonrası veriler bu proje için oluşturulmuş Github sayfasından çekilmiştir. 
+ 2019 yılı öncesi için aylık derlenmiş veriler, 2019 yılı sonrası için de gerçek zamana yakın (NRT) günlük veriler kullanılmıştır. 
```

![image](https://user-images.githubusercontent.com/44377977/174292921-60e364ac-7843-4716-99bc-22093f59e254.png)

![image](https://user-images.githubusercontent.com/44377977/174293100-91d1712f-f23b-4d88-ba38-8019c339ffa8.png)

```diff
+ Deniz Buzu Konsantrasyonu Verisi (Gerçek zamana yakın)/ NSIDC0081: 2015-2022 arası günlük verileri içerir.
```

![image](https://user-images.githubusercontent.com/44377977/174293419-49bb3d4a-0f7b-4915-be69-146b4197bb6b.png)

```diff
+ Deniz Buzu Konsantrasyonu Verisi (Final)/ NSIDC0051: 1978-2021 arası aylık veriyi içerir. Günlük final veriler de var fakat sensörleri ve etiketleri farklı
```

![image](https://user-images.githubusercontent.com/44377977/174293560-21043983-b7c9-44b1-a878-c9cfa5586df7.png)

```diff
+ Deniz Buzu İndeksi Verisi: 1978-2022 arası her ay için tüm yılların genişlik verisi km cinsinden .csv halinde listelenmiştir.
```

![image](https://user-images.githubusercontent.com/44377977/174293610-fde7b136-26a6-4c5e-b878-0fcb12d2d537.png)

![image](https://user-images.githubusercontent.com/44377977/174293827-08a0d0b6-32d5-47b1-9caf-31c6977cd289.png)

```diff
+ Çekilen ızgaralanmış deniz buzu konsantrasyonu verileri görselleştirilmiş hem şekil olarak hem de veri seti olarak kaydedilmiştir. (NSIDC0081-0051)
```

![image](https://user-images.githubusercontent.com/44377977/174294009-e4358694-5820-4d9b-ae41-c116f6ed89c8.png)

```diff
+ Oluşturulan ızgaralanmış Arktik deniz buzu konsantrasyonu verisi ve kullanıma açık deniz buzu indeksi verileriyle sıradan en küçük kareler yöntemine dayanan regresyon tabanlı bir model eğitilmiştir. Tahmin edilen konsantrasyon miktarı ve eğilimin, tespit edilen durumdan farklılıkları bulunmuştur.
```

![image](https://user-images.githubusercontent.com/44377977/174294216-a08e45db-7040-456b-a0ca-3cd7387282aa.png)

```diff
+ Haziran ayındaki deniz buzu tahmin edebilme yeteneğini ölçmek için 2021 yılında aynı aylara ait tahmin ve gerçek değerleri karşılaştıran bir grafik çizilmiştir. Ayrıca tahmin anomalileri ile ilgili de bir şekil çizilmiştir.
```

![image](https://user-images.githubusercontent.com/44377977/174294346-5144faa8-7007-43b6-9eae-1a1e52bfee78.png)

![animatedForecasts](https://user-images.githubusercontent.com/44377977/174294907-12686964-5772-4960-9419-26bc5b3e245b.gif)

## Sonuç

Çalışmadaki deniz buzu konsantrasyonu ve deniz buzu indeksi verileriyle eğitilen model deniz buzu tahminlemede, tahminler ve gerçek değerler karşılaştırıldığında yüksek başarı göstermiştir. Erişilen ve işlenen veriler görselleştirilmiş tahminler grafikleştirilmiştir. Günümüze uyarlanan ve güncellenen modelin başarıyla çalışması ve çıktı üretmesi sağlanıp açık kaynak olarak paylaşılmıştır.

![image](https://user-images.githubusercontent.com/44377977/174294971-b8a8c776-f718-430e-b41d-ebafa57276c6.png)

**Model Özgürlük Derecesi Skoru (Df)**, regresyon modelindeki bağımsız değişkenlerin sayısıdır. Residual Özgürlük Derecesi, tahmin edilen değişkenler ve çıkarılan veri kümesinin toplam gözlem (satır) sayısıdır.Bu modelde, Özgürlük Derecesi çıkarılan değişkenler için 39 ve bağımlı değişken için 1’dir. Bu modelde tahmin gücünü geliştirmek üzere geliştirilmiş değişkenleri ve modelin gücünü gösterir. 

**R Kare Skoru (R- Squared)**, bağımsız değişkenin bağımlı değişkende açıkladığı varyasyon miktarını gösterir.Fakat bu skor modelin yanlılık ya da başarı belirtmez. 
Bu modelde, R Kare Skoru %33. Bu erimedeki değişimlerin %33’ünün açıklanabilir olduğunu gösterir. 

Modelin **Toplam Ortalama Kare Hatası (MSE)** 0’a yakındır. Modelin tahmin performansı bu değer 0’a yaklaştıkça artar. 

Modelin **P Değeri** 0,05'ten büyük ise regresyon çizgisinin eğiminin sıfır olabileceğini, bağımlı ve bağımsız değişkenler arasında anlamlı bir doğrusal ilişkinin bulunmadığını gösterir. Bu modelde, P Değeri 1’dir. Dolasıyla bağımlı ve bağımsız değişkenler arasında kesin ilişki kanıtlanamaz.**

***Bunlar modelin birbiriyle zayıf ilişkileri bulunan değişkenlerle güçlü tahminler yapma yeteneğinde olduğunu kanıtlar niteliktedir. 

Araştırma yapılırken buzullara etki eden nem, atmosfer ve okyanus faktörlerinin birbirleriyle de yakından ilişkili olduğu, buzullar dahil tüm bu ilişkilerin termodinamik ve dinamik prensiplerle açıklandığı ve formülize edildiği gözlemlenmiştir, matematik ve okyanus dalgalarının ve buzulların erimesinin ilişkisi de matematiksel olarak incelenmiş ve ilerideki çalışmaların bu yönde yapılması planlanmıştır.

## Kaynaklar
[1]	Meier, W., Passive microwave products at NSIDC Summary of methods and usage, https://ceres.larc.nasa.gov/documents/STM/2021-09/16_Meier_NSIDC_seaice_CERES_STM_2021.pdf, [Online; erişildi 21-5-2022] (2021).

[2]	Sea Ice Concentrations from Nimbus-7 SMMR and DMSP SSM/I-SSMIS PassiveMicrowave Data, https://nsidc.org/sites/nsidc.org/files/technical-references/NASA%20Technical%20Memorandum%20104647.pdf. [Online; erişildi 21-5-2022] (1997) 

[3]	Chen, D., & Yuan, X. (2004). A Markov Model for seasonal forecast of Antarctic sea ice. Journal of Climate, 17(16), 3156–3168. https://doi.org/10.1175/1520-0442(2004)017

[4]	Serreze, M. C., M. M. Holland, and J. Stroeve (2007), Perspectives on the Arctic’s shrinking sea-ice cover, Science,315(5818), 1533– 1536, doi: 10.1126/science.1139426

[5]	Lindsay, R. W., J. Zhang, A. J. Schweiger, and M. A. Steele (2008), Seasonal predictions of ice extent in the Arctic Ocean, J. Geophys. Res.,113(C2), C02023, doi:10.1029/2007JC004259

[6]	Markus, T., J. C. Stroeve, and J. Miller (2009), Recent changes in Arctic sea ice melt onset, freezeup, and melt season length, J. Geophys.Res.,114, C12024, doi:10.1029/2009JC005436.

[7]	Vancoppenolle, M., Fichefet, T., Goosse, H., Bouillon, S., Madec, G., and Maqueda, M. A. M. (2009). Simulating the mass balance and salinity of Arctic and Antarctic sea ice. 1. Model description and validation. Ocean Model. 27, 33–53. doi: 10.1016/j.ocemod.2008.10.005

[8]	Rousset, Clément & Vancoppenolle, Martin & Madec, Gurvan & Fichefet, Thierry & Flavoni, Simona & Barthélemy, A. & Benshila, Rachid & Chanut, Jérôme & Lévy, Claire & Masson, Sébastien & Vivier, Frédéric. (2015). The Louvain-La-Neuve sea ice model LIM3.6: Global and regional capabilities. Geoscientific Model Development Discussions. 8. 3403-3441. 10.5194/gmdd-8-3403-2015. 

[9]	Stroeve, J. C., V. Kattsov, A. Barrett, M. Serreze, T. Pavlova, M. Holland, and W. N. Meier (2012), Trends in Arctic sea ice extent from CMIP5,CMIP3 and observations, Geophys. Res. Lett.,39, L16502, doi:10.1029/2012GL052676

[10]	Flocco, D., D. Schröder, D. L. Feltham, and E. C. Hunke (2012), Impact of melt ponds on Arctic sea ice simulations from 1990 to 2007, J.Geophys. Res.,117, C09032, doi:10.1029/2012JC008195

[11]	Perovich, D. K., and C. Polashenski (2012), Albedo evolution of seasonal Arctic sea ice, Geophys. Res. Lett.,39, L08501,doi:10.1029/2012GL051432

[12]	Holland, M. M., Blanchard-Wrigglesworth, E., Kay, J., & Vavrus, S. (2013). Initial-value predictability of Antarctic sea ice in the Community Climate System Model 3. Geophysical Research Letters, 40(10), 2121–2124. https://doi.org/10.1002/grl.50410

[13]	Hunke, E. C., Lipscomb, W. H., Turner, A. K., Jeffery, N., and Elliott, S. (2013). CICE: the Los Alamos Sea Ice Model Documentation and Software User’s Manual Version 4.0 LA-CC-06-012.

[14]	Eicken, H. (2013), Ocean science: Arctic sea ice needs better forecasts, Nature,497(7450), 431– 433, doi:10.1038/497431a

[15]	Swart, N. C., J. C. Fyfe, E. Hawkins, J. Abernathey, R. P., Cerovecki, I., Holland, P. R., Newsom, E., Mazloff, M., & Talley, L. D. (2016). Water-mass transformation by sea ice in the upper branch of the Southern Ocean overturning. Nature Geoscience, 9, 596–601. https://doi.org/10.1038/ngeo2749

[16]	Jahn, A., J. E. Kay, M. M. Holland, and D. M. Hall (2016), How predictable is the timing of a summer ice-free Arctic? Geophys. Res. Lett.,43,9113– 9120, doi:10.1002/2016GL070067

[17]	Mortin, J., G. Svensson, R. G. Graversen, M.-L. Kapsch, J. C. Stroeve, and L. N. Boisvert (2016), Melt onset over Arctic sea ice controlled byatmospheric moisture transport, Geophys. Res. Lett.,43, 6636– 6642, doi:10.1002/2016GL069330

[18]	Cox, C. J., Uttal, T., Long, C. N., Stone, R. S., Shupe, M. D., and Starkweather, S. (2016). The role of springtime arctic clouds in determining autumn sea ice extent. J. Clim. 29, 6581–6596. doi: 10.1175/JCLI-D-16-0136.1

[19]	Lee, H. J., Kwon, M. O., Yeh, S. W., Kwon, Y. O., Park, W., Park, J. H., et al. (2017). Impact of poleward moisture transport from the North Pacific on the acceleration of sea ice loss in the Arctic since 2002. J. Clim. 30, 6757–6769. doi: 10.1175/JCLI-D-16-0461.1

[20]	Chi, J., and Kim, H. C. (2017). Prediction of Arctic sea ice concentration using a fully data driven deep neural network. Remote Sens. 9:1305. doi: 10.3390/rs9121305

[21]	Wang, L., Scott, K. A., and Clausi, D. A. (2017). Sea ice concentration estimation during freeze-up from SAR imagery using a convolutional neural network. Remote Sens. 9:408. doi: 10.3390/rs9050408

[22]	Ordoñez, A. C., Bitz, C. M., & Blanchard-Wrigglesworth, E. (2018). Processes controlling Arctic and Antarctic sea ice predictability in the Community Earth System Model. Journal of Climate, 31(23), 9771–9786. https://doi.org/10.1175/jcli-d-18-0348.1

[23]	Community Earth System Model, https://en.wikipedia.org/wiki/Community_Earth_System_Model, [Online; erişildi 22-5-2022].

[24]	Petty, A. A., Webster, M., Boisvert, L., and Markus, T.: The NASA Eulerian Snow on Sea Ice Model (NESOSIM) v1.0: initial model development and analysis, Geosci. Model Dev., 11, 4577–4602, https://doi.org/10.5194/gmd-11-4577-2018, 2018.

[25]	Balibrea-Iniesta, Francisco & Xie, Jiping & García Garrido, Víctor & Bertino, Laurent & Mancho, A. & Wiggins, Stephen. (2019). Lagrangian transport across the upper Arctic waters in the Canada Basin. Quarterly Journal of the Royal Meteorological Society. 145. 76-91. 10.1002/qj.3404. 

[26]	Jun Kim, Y., Kim, H. C., Han, D., Lee, S., and Im, J. (2020). Prediction of monthly Arctic sea ice concentrations using satellite and reanalysis data based on convolutional neural networks. Cryosphere 14, 1083–1104. doi: 10.5194/tc-14-1083-2020

[27]	Handcock, M. S., & Raphael, M. N. (2020). Modeling the annual cycle of daily Antarctic sea ice extent. The Cryosphere, 14(7), 2159–2172. https://doi.org/10.5194/tc-14-2159-2020

[28]	Notz, D., & Baehr, J. (2021). On the origin of discrepancies between observed and simulated memory of Arctic Sea ice. Geophysical Research Letters, 48(11), e2020GL091784. https://doi.org/10.1029/2020GL091784Goosse, H., & Zunz, V.

[29]	Doddridge, E. W., Marshall, J., Song, H., Campin, J.-M., & Kelley, M. (2021). Southern Ocean heat storage, reemergence, and winter sea ice decline induced by summertime winds. Journal of Climate, 34(4), 1403–1415.

[30]	Petty, Alek, Sea Ice Prediction Project,  https://github.com/akpetty/SeaIcePrediction. [Online; erişildi 22-5-2022].

[31]	Öztürk, Gizem, Deniz Buzu Tahmini Projesi, https://github.com/ozturkgizem/042422. [Online; erişildi 22-5-2022].

[32]	Cavalieri, D. J., C. L. Parkinson, P. Gloersen, and H. J. Zwally. 1996, updated yearly. Sea Ice Concentrations from Nimbus-7 SMMR and DMSP SSM/I-SSMIS Passive Microwave Data, Version 1. [Indicate subset used]. Boulder, Colorado USA. NASA National Snow and Ice Data Center Distributed Active Archive Center. doi: https://doi.org/10.5067/8GQ8LZQVL0VL. [Online; erişildi 22-5-2022].

[33]	Meier, W. N., J. S. Stewart, H. Wilcox, M. A. Hardman, and D. J. Scott. 2021. Near-Real-Time DMSP SSMIS Daily Polar Gridded Sea Ice Concentrations, Version 2. [Indicate subset used]. Boulder, Colorado USA. NASA National Snow and Ice Data Center Distributed Active Archive Center. doi: https://doi.org/10.5067/YTTHO2FJQ97K. [Online; erişildi 22-5-2022].

[34]	Sea Ice Index Data, https://nsidc.org/data/seaice_index/archives. [Online; erişildi 22-5-2022].

[35]	freeCodeCamp, How to Read a Regression Table, https://www.freecodecamp.org/news/https-medium-com-sharadvm-how-to-read-a-regression-table-661d391e9bd7-708e75efc560/#:~:text=Degrees%20of%20freedom%20(df)&text=Since%20we%20only%20consider%20GRE,and%20the%20constant%20are%20estimated.. [Online; erişildi 22-5-2022].


***:cowboy_hat_face: 
resource code: [30]	Petty, Alek, Sea Ice Prediction Project,  https://github.com/akpetty/SeaIcePrediction. [Online; erişildi 22-5-2022].***
