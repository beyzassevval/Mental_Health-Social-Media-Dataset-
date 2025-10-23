# Mental_Health-Social-Media-Dataset-

🧠 Mutluluk Endeksi Tahmini: Sosyal Medya ve Yaşam Tarzı AnaliziBu proje, ekran süresi,
stres, uyku ve egzersiz gibi yaşam tarzı faktörlerine dayanarak bir kişinin Mutluluk Endeksini (Happiness Index)
tahmin eden güçlü bir makine öğrenimi çözümüdür. 

Gelişmiş ensemble yöntemleri ve kapsamlı özellik mühendisliği ile yüksek doğrulukta bir tahmin modeli oluşturulmuştur.

🎯 Temel Proje ÖzellikleriVeri Seti: 
Mental Sağlık ve Sosyal Medya Dengesi Veri Seti (Mental_Health_and_Social_Media_Balance_Dataset.csv).
Hedef: Happiness_Index(1-10) skorunu tahmin etmek.
Özellik Mühendisliği: Etkileşimler (Stress_Sleep_Ratio, Screen_Stress) ve kompozit skorlar (Health_Score, Lifestyle_Balance) ile model gücü artırıldı.
🛠️ Kullanılan Modeller ve Ensemble YöntemleriÇeşitli regresyon modelleri eğitilmiş ve Stacking Ensemble metodu ile birleştirilmiştir.
ModelR² Skoru (Test)RMSERandomForest0.66330.9096Stacking Ensemble0.64870.9292CatBoost0.62630.9583XGBoost0.57501.0220
🏆 En İyi Performans: RandomForest Regressor ($R^2 = 0.6633$).

💡 Kritik Bulgular: En Önemli ÖzelliklerXGBoost modeline göre mutluluk endeksini en çok etkileyen faktörler:Stress_Sleep_Ratio (Stres/Uyku Oranı):
En güçlü tahmin edici.High_Screen (Yüksek Ekran Süresi): Günlük 6+ saat ekran kullanımı.Screen_Stress (Ekran Süresi $\times$ Stres): İki negatif faktörün birleşimi.
Stress_Squared (Stresin Karesi): Stresin doğrusal olmayan (büyük) etkisi.
🚀 İnteraktif Tahmin SistemiProje, Jupyter Notebook içerisinde kullanıcıdan aldığı güncel yaşam tarzı verilerine dayanarak anlık Mutluluk Endeksi Tahmini yapar ve kişiye özel yaşam tarzı önerileri sunar.

Örnek Tahmin ÇıktısıÖrnek Yaşam TarzıNihai Tahmin (Stacking)Genel DeğerlendirmeYüksek Ekran (10 saat), Düşük Uyku (1), Yüksek Stres (9)5.83Yaşam tarzı değişikliği gerekiyor.Yüksek Uyku (9), Yüksek Egzersiz (4), Orta Stres (6)9.03Mutluluk seviyeniz çok iyi!⚙️ Kurulum ve ÇalıştırmaDepoyu klonlayın.
Gerekli kütüphaneleri kurun:Bashpip install pandas numpy scikit-learn xgboost lightgbm catboost
Mental_Health.ipynb dosyasını çalıştırın. Tüm hücreleri sırayla çalıştırdığınızda model eğitilir ve interaktif tahmin sistemi başlar.
