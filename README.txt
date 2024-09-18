Bitcoin Fiyat Tahmin Projesi

Bitcoin fiyat tahminleri üzerine gerçekleştirdiğim veri analizi ve makine öğrenimi projesini adım adım paylaşacağım.

İlk olarak, veri ön işleme sürecine odaklandım. Bitcoin fiyat verisini başarılı bir şekilde yükledim, eksik verileri temizledim ve gereksiz sütunları kaldırdım. Sonrasında veriyi ölçeklendirdim ki, bu adım model performansı açısından kritik bir rol oynadı. Özellikle StandardScaler kullanarak veriyi normalize ettim, böylece modellerin kararlı ve daha iyi sonuçlar üretmesini sağladım. Bu aşamada, veriyi düzgün hazırlamak makine öğrenimindeki başarı için çok önemli bir adımdı.

Veriyi görselleştirirken, Bitcoin fiyatlarının zaman içindeki değişimini grafikler ile ortaya koydum. SMA (Basit Hareketli Ortalama) kullanarak Bitcoin'in fiyat hareketlerini analiz ettim. Bu, alım-satım sinyalleri oluşturmak açısından değerli bir strateji oldu. Piyasa trendlerini doğru bir şekilde takip edebilmek adına, bu hareketli ortalama yöntemi finansal veri analizi için güçlü bir araç sundu.

Ardından, Linear Regression ve RandomForestRegressor algoritmalarını uyguladım ve karşılaştırdım. Model performanslarını değerlendirmek için Mean Squared Error (MSE) metriğini kullandım. Sonuçlar, Random Forest modelinin Linear Regression’a kıyasla çok daha başarılı olduğunu gösterdi. Bu noktada, doğru algoritma seçiminin ne kadar önemli olduğunu bir kez daha gözlemledim. Ancak, daha fazlasını araştırmak ve farklı yaklaşımlar denemek amacıyla gözetimsiz öğrenme modellerine geçiş yaptım.

KMeans algoritmasını uygulayarak veri kümesini farklı gruplara ayırdım. Bu yöntemle, veri üzerinde daha derin bir analiz yapma fırsatım oldu. KMeans’in, Bitcoin fiyatlarındaki farklı paternleri ve gruplamaları keşfetmek açısından sunduğu faydalar, bu projeye yeni bir perspektif kazandırdı. Gözetimli ve gözetimsiz öğrenme yöntemlerini birlikte kullanarak sonuçları kıyaslamak, veri analizi yeteneklerimi geliştirirken aynı zamanda analitik bakış açımı da genişletti.

Sonuç olarak, bu proje boyunca veri işleme, görselleştirme ve modelleme aşamalarında gösterdiğim detaylı çalışma, bana güzel bir deneyim kattı. Veriyi hazırlama aşamasından model değerlendirmesine kadar her adımda titizlikle ilerleyerek, makine öğrenmesi ve finansal veri analizi üzerine sağlam bir altyapı oluşturduğumu düşünüyorum. Özellikle, farklı algoritmaları uygulayıp sonuçları karşılaştırmam, veriye olan bakış açımı geliştirmemi sağladı.

Bu projenin bana kattığı deneyim, gelecekteki makine öğrenimi çalışmalarımda kullanabileceğim bir rehber niteliğinde oldu. Projeyi sonuçlandırırken öğrendiğim her şeyin, analitik yetkinliğimi ve problem çözme becerilerimi ileriye taşıdığını düşünüyorum.

İçindekiler

Proje Amacı
Veri Kümesi
Veri Ön İşleme
Modelleme
Gözetimli Öğrenme
Gözetimsiz Öğrenme
Sonuçlar ve Değerlendirme
Kurulum ve Kullanım
Proje Amacı

Bu proje, Bitcoin'in fiyat hareketlerini tahmin etmek ve çeşitli öğrenme algoritmaları kullanarak model performansını değerlendirmek için geliştirilmiştir. Hem gözetimli hem de gözetimsiz öğrenme yöntemleri kullanılarak veriler üzerinde analiz yapılmıştır.

Veri Kümesi

Veri kümesi, 2018'den 2024'e kadar olan Bitcoin fiyat verilerini içermektedir. Fakat ben Kısıtlı RAM imkanından dolayı 30000 satırlık veri ile çalıştım gelecekte daha rahat bir şekilde kalan verileri dahil ederek çalışılabilir. Veriler şunları içerir:

Açılış fiyatı
Yüksek fiyat
Düşük fiyat
Kapanış fiyatı
İşlem hacmi

Veri Ön İşleme

Veri Yükleme: Veriler CSV formatında yüklenmiştir.
Eksik Veriler: Eksik veriler kontrol edilip temizlenmiştir.
Özellik Seçimi ve Ölçekleme: Özellikler seçilip normalleştirilmiştir.
Hedef Değişken: Kapanış fiyatının bir önceki güne göre yüksek olup olmadığına göre etiketlenmiştir.

Modelleme

Gözetimli Öğrenme
Linear Regresyon:
Model: Linear Regression
Performans: Ortalama Kare Hata (MSE) hesaplandı.

Random Forest Regressor:
Model: RandomForestRegressor
Performans: Ortalama Kare Hata (MSE) hesaplandı.

Random Forest Classifier:
Model: RandomForestClassifier
Performans: Doğruluk Skoru ve ROC Eğrisi hesaplandı.

XGBoost:
Model: XGBClassifier
Performans: Doğruluk Skoru ve Sınıflandırma Raporu hesaplandı.

Gözetimsiz Öğrenme
KMeans Kümeleme:
Model: KMeans
Kümeler belirlendi ve Silhouette Skoru hesaplandı.

DBSCAN Kümeleme:
Model: DBSCAN
Hiperparametre optimizasyonu yapıldı ve kümeler belirlendi.
Sonuçlar ve Değerlendirme

Gözetimli Öğrenme: Farklı modellerin performansları karşılaştırıldı ve en uygun model belirlendi.
Gözetimsiz Öğrenme: Kümeleme sonuçları ve model performansı değerlendirildi.
