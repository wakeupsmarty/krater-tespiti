# Proje Günlüğü — Ay Krateri Tespiti

---
## 18.05.2026

nlp kullandığım projemi değiştirdim bunun yerine yolo kullandığım bir projeye başladım . bunun için de convolution , neural network,maxpooling ,flatten ve danse kavramlarını öğrendim bir yatay çizi göreselinin algılandığı sayı dizisinin görüntüsünü öğrendim.

Kullanılan kaynak: chatgpt 

Sorun: öğrenme aşamasındayım bir sorunum yok

Sonraki adım: softmax ve backpropagation öğrenmek. dataset ve görselleri yüklemek

## 23.05.2026

**Ne yaptım?**
Proje konusunu belirledim: YOLOv8 ile ay krateri tespiti. Kaggle'da LU3M6TGT veri setini buldum (8756 eğitim, 1545 doğrulama görüntüsü, YOLO formatında). Google Colab'da yeni bir notebook oluşturdum ve GPU (T4) etkinleştirdim.

**Kullanılan AI aracı / kaynak:**
Claude (Anthropic) — kurulum adımları, hata çözümü ve kod yapısı için yardım aldım.

**Karşılaştığım sorun ve nasıl çözdüm?**
İlk indirdiğim zip dosyası bozuk çıktı ("End-of-central-directory signature not found" hatası). Sorunun sebebi dosyanın düzgün indirilmemiş olmasıydı. Kaggle API kullanarak (`kaggle datasets download`) doğrudan indirince sorun çözüldü.

**Bir sonraki adım:**
data.yaml path hatalarını düzeltmek ve model eğitimini başlatmak.

---

## 23.05.2026 (devam)

**Ne yaptım?**
data.yaml dosyasındaki path'lerin başka bir bilgisayara ait olduğunu fark ettim. Python ile dosyayı güncelleyerek Colab'daki doğru dizin yollarını yazdım. Ardından YOLOv8n modelini 50 epoch ile eğitmeye başladım.

**Kullanılan AI aracı / kaynak:**
Claude — data.yaml'ın neden hata verdiğini anlamak ve düzeltme kodunu yazmak için kullandım.

**Karşılaştığım sorun ve nasıl çözdüm?**
data.yaml içindeki `train` ve `val` path'leri `/home/super/tmp_datasets/...` olarak geliyordu, oysa Colab'da dosyalar `/content/dataset/...` altında. YAML dosyasını Python ile yeniden yazdım.

**Bir sonraki adım:**
Eğitim sonuçlarını (mAP, loss grafikleri) incelemek ve test görüntüleri üzerinde tahmin yapmak.

---

## 24.05.2026

**Ne yaptım?**
Eğitim tamamlandı. mAP50 ve mAP50-95 değerlerini inceledim. En iyi model ağırlıklarını (`best.pt`) kullanarak test görüntüleri üzerinde tahmin yaptım.

**Kullanılan AI aracı / kaynak:**
Claude — sonuçları yorumlamak ve README yazmak için kullandım.

**Bir sonraki adım:**
GitHub repo oluşturmak ve dosyaları yüklemek.

---

## 24.05.2026

**Ne yaptım?**
GitHub reposu oluşturdum. README.md, gunluk.md, requirements.txt ve notebook dosyasını yükledim. Sunum dosyasını hazırladım.

**Kullanılan AI aracı / kaynak:**
Claude — README ve sunum içeriği için kullandım.


**Bir sonraki adım:**
GUZEM'e zip olarak yüklemek.
