🧠 Obesity Level Classification using Random Forest

Bu proje, bireylerin fiziksel özellikleri ve yaşam alışkanlıklarına dayanarak obezite seviyelerini tahmin etmeye yönelik bir makine öğrenmesi uygulamasıdır. Python ve Scikit-Learn kütüphanesi kullanılarak geliştirilmiş, çok sınıflı sınıflandırma problemi Random Forest algoritması ile çözülmüştür.

📁 Proje İçeriği

Veri Kümesi: ObesityDataSet_raw_and_data_sinthetic.csv
Hedef: NObeyesdad (7 sınıflı obezite seviyesi)
Model: Random Forest Classifier
Ek Adımlar: Veri önişleme, SMOTE ile sınıf dengesi, ROC analizi, Feature Importance, PCA
🎯 Problem Tanımı

Bu proje kapsamında amaç; yaş, boy, kilo, beslenme alışkanlıkları, fiziksel aktivite gibi verilerden yola çıkarak bireylerin obezite düzeylerini aşağıdaki 7 sınıftan birine doğru şekilde tahmin etmektir:

Insufficient_Weight
Normal_Weight
Overweight_Level_I
Overweight_Level_II
Obesity_Type_I
Obesity_Type_II
Obesity_Type_III
📊 Kullanılan Yöntemler ve Araçlar

Aşama	Açıklama
Veri Önişleme	Label Encoding, One-Hot Encoding, BMI Hesaplama
Normalizasyon	StandardScaler kullanılarak tüm sayısal özellikler normalize edildi
Dengeleme	SMOTE algoritması ile sınıf örnek sayıları eşitlendi
Modelleme	OneVsRestClassifier + RandomForestClassifier
Performans Değerlendirme	Confusion Matrix, Accuracy, F1-Score, ROC AUC
Boyut İndirgeme	PCA ile 95% varyans için optimum bileşen seçildi
📈 Performans Sonuçları

Doğruluk (Accuracy): 0.9905
F1-Skor (Tüm Sınıflar): 0.97 - 1.00
ROC-AUC: Tüm sınıflar için 1.00
PCA'lı Model Doğruluğu: 0.8723 (Bu nedenle PCA uygulanmamıştır)
📊 Görseller

Aşağıdaki grafikler proje çıktılarına örnektir:

📌 Sınıf Dağılımı: Dengesiz sınıfları görselleştirir
📌 Korelasyon Matrisi: Özellikler arası ilişki
📌 ROC Eğrileri: Modelin sınıf ayırt etme gücü
📌 Öznitelik Önem Dereceleri: BMI, Weight, Age, Height en önemli faktörler
📌 Confusion Matrix: Hangi sınıf hangi sınıfla karıştırılmış?
📍 Tüm görseller ve detaylı açıklamalar proje notebook dosyasında bulunmaktadır.
🛠 Kurulum

Projeyi çalıştırmak için aşağıdaki adımları takip edin:

git clone https://github.com/kullaniciadi/obesity-rf-classification.git
cd obesity-rf-classification
pip install -r requirements.txt
python obesity_rf_model.py
Jupyter ile çalışacaksanız .ipynb dosyasını çalıştırabilirsiniz.

📌 Sonuç ve Öneriler

Random Forest algoritması, sınıflar arası yüksek doğruluk ve denge sağlamıştır.
ROC eğrileri ve AUC değerleri, sınıf ayrım başarısının güçlü olduğunu göstermektedir.
PCA, doğruluk oranını düşürdüğü için modelde tercih edilmemiştir.
BMI, Weight, Age, FAF gibi öznitelikler obezite seviyesinin tahmininde anahtar rol oynamaktadır.
Bu model, klinik karar destek sistemlerinde veya sağlık uygulamalarında risk sınıflandırması amacıyla kullanılabilir.
🤝 Katkıda Bulun

Pull request gönderebilir, fork ederek geliştirmelere katkı sağlayabilirsiniz.

📄 Lisans

Bu proje MIT lisansı ile lisanslanmıştır.

