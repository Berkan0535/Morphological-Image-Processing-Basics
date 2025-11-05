## 📘 README.md

# 🧠 Morphological Image Processing Basics

### 📸 OpenCV ile Morfolojik Görüntü İşleme

Bu Jupyter Notebook, **dijital görüntü işleme** sürecinde kullanılan temel **morfolojik işlemleri (morphological operations)** öğretmek amacıyla hazırlanmıştır.
Bu teknikler, **gürültü giderme, kenar tespiti ve şekil analizi** gibi birçok görüntü çözümleme uygulamasının temelini oluşturur.

---

## 🧩 İçerik Başlıkları

1. **Erosion (Aşınma)**

   * Beyaz piksellerin küçülmesini sağlar.
   * Görüntüdeki ince detayları ortadan kaldırmak veya küçük beyaz noktaları silmek için kullanılır.
   * Örnek kullanım:

     ```python
     erosion = cv2.erode(img, kernel, iterations=1)
     ```

2. **Dilation (Genişleme)**

   * Erosion’un tersidir. Beyaz bölgeleri büyütür.
   * Kırık kenarları birleştirmek veya boşlukları doldurmak için kullanılır.

     ```python
     dilation = cv2.dilate(img, kernel, iterations=1)
     ```

3. **Opening (Açma)**

   * **Erosion → Dilation** işlemlerinin ardışık uygulanmasıdır.
   * Amaç: Küçük beyaz gürültüleri temizlemek.

     ```python
     opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel)
     ```

4. **Closing (Kapama)**

   * **Dilation → Erosion** işlemlerinin ardışık uygulanmasıdır.
   * Amaç: Küçük siyah boşlukları kapatmak.

     ```python
     closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel)
     ```

5. **Morphological Gradient (Gradyan)**

   * Görüntüdeki kenar bölgelerini belirlemek için erosion ve dilation farkını kullanır.
   * Kenar tespitinde sıklıkla uygulanır.

     ```python
     gradient = cv2.morphologyEx(img, cv2.MORPH_GRADIENT, kernel)
     ```

---

## 🛠️ Kullanılan Teknolojiler

* **Python 3.x**
* **OpenCV (cv2)**
* **NumPy**

---

## 🚀 Çalıştırma

1. Gerekli kütüphaneleri yükleyin:

   ```bash
   pip install opencv-python numpy
   ```

2. Notebook’u açın:

   ```bash
   jupyter notebook Morphological-Image-Processing-Basics.ipynb
   ```

3. Hücreleri sırayla çalıştırarak farklı morfolojik işlemleri gözlemleyin.

---

## 🎯 Öğrenme Hedefleri

* Morfolojik işlemlerin dijital görüntüler üzerindeki etkilerini anlamak
* Gürültü giderme ve kenar tespiti mantığını kavramak
* OpenCV fonksiyonlarını kullanarak **erozyon, genişleme, açma, kapama ve gradyan** işlemlerini uygulayabilmek

---

## 📷 Örnek Görseller (İsteğe Bağlı)

| İşlem        | Açıklama                   |
| ------------ | -------------------------- |
| **Erosion**  | Beyaz alanları küçültür.   |
| **Dilation** | Beyaz alanları genişletir. |
| **Opening**  | Gürültüleri temizler.      |
| **Closing**  | Boşlukları kapatır.        |
| **Gradient** | Kenarları vurgular.        |

---

## 🧠 Not

Bu çalışma, dijital görüntü çözümlemenin **morfolojik analiz** aşamasına giriş niteliğindedir.
Bir sonraki adım olarak **edge detection (Canny, Sobel, Laplacian)** gibi ileri seviye tekniklere geçilebilir.

---
