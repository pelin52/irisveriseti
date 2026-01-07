# 🌸 Iris Veri Seti ile KNN ve Yapay Sinir Ağı Sınıflandırma Projesi

## 📌 Veri Seti Açıklaması

Bu projede **Iris Flower Dataset** kullanılmıştır. Veri seti 150
gözlemden ve 4 bağımsız değişkenden oluşur:

  Özellik         Açıklama
  --------------- --------------------------------------------
  SepalLengthCm   Çanak yaprağı uzunluğu (cm)
  SepalWidthCm    Çanak yaprağı genişliği (cm)
  PetalLengthCm   Taç yaprağı uzunluğu (cm)
  PetalWidthCm    Taç yaprağı genişliği (cm)
  Species         Çiçek türü (Setosa, Versicolor, Virginica)

Her türden 50 örnek bulunmaktadır. Veri seti Kaggle API kullanılarak
indirilmiş ve `Iris.csv` dosyasından okunmuştur.

------------------------------------------------------------------------

## 🧠 Model Mimarileri

### 🔹 KNN (K-Nearest Neighbors)

-   Özellik matrisi: X = 4 özellik
-   Hedef değişken: Species
-   Eğitim/Test oranı: %80 / %20
-   Komşu sayısı: `k = 3`
-   Performans metrikleri:
    -   Accuracy
    -   Confusion Matrix
    -   Classification Report (Precision, Recall, F1-score)

------------------------------------------------------------------------

### 🔹 Yapay Sinir Ağı (Neural Network)

Model Keras kullanılarak oluşturulmuştur.

  Katman           Nöron Sayısı   Aktivasyon
  ---------------- -------------- ------------
  Giriş Katmanı    4              \-
  Gizli Katman 1   16             ReLU
  Gizli Katman 2   8              ReLU
  Çıkış Katmanı    3              Softmax

-   Optimizer: Adam\
-   Loss: categorical_crossentropy\
-   Epoch: 50\
-   Batch Size: Varsayılan


------------------------------------------------------------------------

## 📈 Başarı Metrikleri

### KNN Modeli

  Metric      Değer
  ----------- --------
  Accuracy    \~0.97
  Precision   Yüksek
  Recall      Yüksek
  F1-Score    Yüksek

Confusion Matrix görseli:

![KNN Confusion Matrix](images/knn_cm.png)

------------------------------------------------------------------------

### Neural Network Modeli

  Metric          Değer
  --------------- --------
  Test Accuracy   \~0.98
  Loss            Düşük

Confusion Matrix görseli:

![NN Confusion Matrix](images/nn_cm.png)

------------------------------------------------------------------------

## ▶️ Google Colab Ortamı

Bu proje aşağıdaki bağlantı üzerinde çalıştırılmıştır:

https://colab.research.google.com/drive/1RLawnyZOQ1VZ12I4ovjzDiSRPKUd75Yz#scrollTo=W9Qrw8rWkRwB
