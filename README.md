# 🚗 Araç Özellikleri Üzerinden Fiyat Tahmini (Linear, Ridge, Lasso Regression)

Bu proje, bir araç veri setindeki teknik ve kategorik özellikleri kullanarak araçların **MSRP (üretici tarafından önerilen satış fiyatı)** değerini tahmin etmeyi amaçlar.  
Projede **doğrusal regresyon modelleri (Linear, Ridge, Lasso)** kullanılmış ve farklı regularization teknikleri karşılaştırılmıştır.

---

## 📊 Proje Özeti

Veri seti, araçlara ait **motor, yakıt tipi, şanzıman, çekiş tipi, kapı sayısı, marka** gibi teknik özellikleri içerir.  
Amaç: Bu değişkenleri kullanarak araç fiyatlarını tahmin etmek.

Proje adımları:
1. **Veri Temizleme (Data Cleaning)**
   - Eksik değerlerin median veya mode ile doldurulması  
   - Gerekli sütunların silinmesi veya düzenlenmesi  

2. **Veri Dönüştürme (Encoding)**
   - `Make` sütunu için **Target Encoding**  
   - `Engine Fuel Type`, `Transmission Type`, `Driven Wheels`, `Vehicle Size`, `Vehicle Style` sütunları için **One-Hot Encoding**

3. **Ölçekleme (Scaling)**
   - Tüm sayısal değişkenler **StandardScaler** ile normalize edilmiştir.

4. **Modelleme (Model Training)**
   - **Linear Regression**
   - **Ridge Regression**
   - **Lasso Regression**

5. **Model Değerlendirme**
   - Ortalama Mutlak Hata (MAE)  
   - Ortalama Kare Hata (MSE)  
   - R² Skoru

---

## 🧠 Kullanılan Teknolojiler

- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

## ⚙️ Model Sonuçları (Örnek)

| Model | MAE | MSE | R² |
|--------|------|------|------|
| Linear Regression | 10,736 | 563,027,450 | 0.7867 |
| Ridge Regression | 10,738 | 562,972,172 | 0.7868 |
| Lasso Regression | 10,918 | 659,248,209 | 0.7503 |

🔹 Ridge, klasik lineer modele çok yakın sonuç verirken;  
🔹 Lasso modeli bazı katsayıları sıfırlayarak model karmaşıklığını azaltmıştır.

---

## 🧩 Gelecek Çalışmalar

- **Log Dönüşümü (Log Transform):** MSRP değerleri log ölçeğine alınarak doğrusal ilişki güçlendirilebilir.  
- **Feature Engineering:** HP/Cylinder oranı, şehir/otoban yakıt oranı gibi yeni özellikler eklenebilir.  
- **Non-Linear Modeller:** Random Forest veya XGBoost gibi modellerle doğruluk artırılabilir.

---
