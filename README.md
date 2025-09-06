Veri Bilimi Projesi: Hastaların Tedavi Süresi Tahmini
Bu proje, sağlık verilerini kullanarak hastaların tedavi sürelerini tahmin etmeyi amaçlayan kapsamlı bir veri analizi ve makine öğrenmesi çalışmasıdır. Veri keşfi, ön işleme, özellik mühendisliği ve modelleme adımları, sürecin her aşamasını detaylı bir şekilde göstermektedir.

Genel Bakış
Bu Jupyter Notebook (Untitled7.ipynb), "Talent_Academy_Case_DT_2025.xlsx" adlı veri setini temel alarak oluşturulmuştur. Projenin ana hedefi, hasta verilerine dayanarak TedaviSuresi değişkenini doğru bir şekilde tahmin eden bir makine öğrenmesi modeli geliştirmektir.

Kullanılan Kütüphaneler
Projede veri analizi ve modelleme için aşağıdaki popüler Python kütüphaneleri kullanılmıştır:

pandas: Veri manipülasyonu ve analizi.

numpy: Sayısal işlemler ve hesaplamalar.

matplotlib & seaborn: Veri görselleştirme.

scikit-learn: Makine öğrenmesi algoritmaları ve değerlendirme metrikleri.

Proje Adımları
Proje, aşağıdaki adımları içermektedir:

1. Veri Keşfi ve Ön İşleme
Veri seti yüklenmiş ve ilk bakışta genel yapısı, sütun tipleri ve eksik değerler incelenmiştir.

Sütun isimleri, daha anlaşılır ve kod dostu bir hale getirilmek için yeniden düzenlenmiştir.

Gereksiz sütunlar veri setinden çıkarılmıştır.

Kayıp veriler tespit edilmiş ve en uygun yöntemlerle doldurulmuştur.

'Yaş' sütunundaki aykırı değerler incelenmiş ve mantıksal sınırlar dahilinde ele alınmıştır.

2. Özellik Mühendisliği
'Yaş' sütunundan yeni bir özellik olan Yaş_Grubu türetilmiştir.

'KronikHastalik', 'Alerji' ve 'Tanilar' gibi metinsel veriler, makine öğrenmesi modelinin kullanabileceği sayısal özelliklere dönüştürülmüştür. Bu adımda, her bir hastalığın veya tanının varlığını gösteren ikili (binary) sütunlar oluşturulmuştur.

3. Modelleme ve Değerlendirme
Kategorik değişkenler (örneğin Cinsiyet, KanGrubu, Bolum) One-Hot Encoding ve Label Encoding yöntemleriyle sayısal formata dönüştürülmüştür.

Tahmin modeli olarak Linear Regression kullanılmıştır.

Modelin performansı Ortalama Mutlak Hata (MAE) ve Kök Ortalama Kare Hata (RMSE) gibi metriklerle değerlendirilmiştir.

Sonuç
Bu çalışma sonucunda, ham veriden işlenmiş ve modellemeye hazır hale getirilmiş bir veri seti elde edilmiştir. Bu veri seti, processed_dataset.csv ve processed_dataset.xlsx dosyaları olarak kaydedilmiştir. Geliştirilen model, hasta özelliklerine dayanarak tedavi süresini tahmin etme yeteneğine sahiptir.