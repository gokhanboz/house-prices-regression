🏠 House Prices: Advanced Regression Techniques

📘 Proje Hakkında

Bu proje, Kaggle'daki "House Prices: Advanced Regression Techniques" yarışması kapsamında geliştirilmiştir. Amaç, konut özelliklerinden yola çıkarak ev fiyatlarını tahmin eden etkili bir regresyon modeli oluşturmaktır.

🔧 Uygulanan Adımlar

1. Veri Yükleme ve Temizleme

Eksik değer analizi yapıldı.

Kategorik değişkenler "None" veya mod değeri ile dolduruldu.

Sayısal veriler 0, ortanca veya mahalle medyanı gibi mantıklı değerlerle tamamlandı.

2. Özellik Mühendisliği (Feature Engineering)

Aşağıdaki yeni sütunlar oluşturuldu:

TotalSF = TotalBsmtSF + 1stFlrSF + 2ndFlrSF

TotalBath = FullBath + 0.5HalfBath + BsmtFullBath + 0.5BsmtHalfBath

HasPool, HasFireplace, HasGarage gibi binary sütunlar

3. One-Hot Encoding

Tüm kategorik değişkenler sayısallaştırıldı.

train/test veri setleri hizalandı.

4. Modelleme

Aşağıdaki modeller denenmiştir:

Ridge Regression

Lasso Regression

Random Forest

XGBoost (en başarılı model)

5. Ensemble

Ridge ve Lasso tahminleri ortalanarak basit bir ensemble modeli denendi.

🧠 Sonuçlar

İlk skor (baseline): 11.44

XGBoost modelinden sonra: 1.54

Feature engineering + XGBoost: 0.13379 (RMSLE)

🗂 Dosya Yapısı

train.csv, test.csv → ham veriler

submission_xgboost_features.csv → son tahmin sonucu

notebook.ipynb veya main.py → tüm analiz ve modelleme adımları

README.md → proje özeti

🚀 Kullanılan Araçlar

Python (pandas, numpy, scikit-learn, xgboost)

Jupyter Notebook

Kaggle veri seti

📌 Notlar

Bu proje, regresyon problemleri için veriye dayalı düşünme, özellik mühendisliği ve model tuning becerilerini geliştirmek amacıyla yapılmıştır.