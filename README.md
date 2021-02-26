# Covid19_project

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)  [![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)  


Bu projede 3  farklı model kullanarak eldeki verilerden  bir sonraki gün için yaşanacak can kaybı tahmini yaptım.Kullandığım modeller sırasıyla;

1)Prophet modeli:

Facebook veri bilimi ekibi tarafından geliştirilen açık kaynak kodlu bir tahminleme uygulamasıdır.Doğrusal olmayan zaman serisi verileri üzerinden yıllık, dönemlik, haftalık, günlük tahminlerde bulunmayı sağlayan prosedürler içerir. Prophet modeli veri kayıpları ve uç değerleri başarılı bir şekilde ele alma kabiliyetine sahiptir. Model, günümüzde Facebook bünyesindeki pek çok uygulamada aktif olarak kullanılmaktadır.Prophet iki özellikli bir veri kümesini girdi olarak alır.  Bu özelliklerden ilki olan ds zaman
damgasıdır ve Python dilindeki veri işleme kütüphanesi olan pandas tarafından ele alınabilecek zaman formatlarını destekler. Diğer özellik olan y ise tahmine konu olan nümerik ölçüm değeridir. İçerisinde ds ve y değerleri içeren veri seti ile eğitilen model farklı periyotlarda tahminler üretebilir. Prophet modelinin işleyişindeki sezgisel yaklaşım verinin detaylarına boğulmadan etkili tahminler oluşturabilmeyi sağlar.

 ![prophet_teori](https://user-images.githubusercontent.com/48547417/109233402-e4cabd80-77da-11eb-9b44-e1e74adc0e8c.PNG) 

Model üzerinden yapılan tarih bazlı gelecek tahminleri bir değer aralığı olarak üretilir. Muhtemel tahmin değeri yhat, tahmin üst
sınırı yhat_upper ve tahmin alt sınırı yhat_lower değerleri ile bir değer bandı olarak üretilir

MOVİNG AVERAGE  ==>Ortalama alma yöntemi:
      
 "Hareketli ortalama" terimi, verilerdeki mevcut herhangi bir eğilim veya model hakkında içgörüler elde etmek için verilerde gözlemlenen dalgalanmayı yumuşatan teknik analiz  tekniğini ifade eder. Veri deseni daha sonra geleceği tahmin etmek için bir gösterge olarak kullanılır. Hareketli ortalama, temel olarak üç türde olabilir:Bu projede hareketli ortalama yaklaşımlarından SMA ve EMA yöntemlerini kullandım.

2)Simple Moving Average:



![SMA](https://user-images.githubusercontent.com/48547417/109236292-61ac6600-77e0-11eb-94bc-44f94643a93f.PNG)

3)Exponential Moving Average: 
SMA 'ya göre daha duyarlı bir model olup en son oluşan değişikliklere daha duyarlıdır.
![EMA](https://user-images.githubusercontent.com/48547417/109236441-afc16980-77e0-11eb-9dda-00250b75c7f6.PNG)

Kodumdaki modelleri hata oranları aşağıdaki gibidir ve histogramı mevcuttur 
+ Mean Absolute Errors (MAE): {'Prophet': 9.755691660019027, 'SMA_3': 4.691954022988506, 'EMA_3': 4.534847019016072} 

![Error_RatePNG](https://user-images.githubusercontent.com/48547417/109237045-e946a480-77e1-11eb-8dcd-b484d65699b6.PNG)

#English-Readme

## Technologies
Project is created with:
* Python version: 3.7.3
