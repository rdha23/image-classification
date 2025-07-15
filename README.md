# 🧠 Image Classification of Traditional Foods

Klasifikasi citra makanan tradisional khas Kalimantan Selatan menggunakan model deep learning **EfficientNetB0** dan **InceptionV3**.

## 📁 Struktur Dataset
Pastikan dataset tersimpan dengan struktur seperti berikut:
<pre> <code>
data/
├── soto-banjar/
│   ├── soto-banjar-1.jpg
│   ├── soto-banjar-2.jpg
│   └── ...
├── ketupat-kandung/
│   ├── ketupat-kandung-1.jpg
│   └── ...
└── dll.
  </code> </pre>

## 🚀 Cara Menggunakan

1. Buat folder data di root utama
2. Download dataset pada link berikut:
  👉 [Google Drive Dataset](https://drive.google.com/drive/folders/105dWHSnwdJ_1UNymu-DX8GZISRFoGo_n?usp=sharing)
4. Pastikan path datasetnya seperti berikut: data/soto-banjar/soto-banjar-1.jpg 
5. Buka path folder project yang berisi data dan model 
6. Buka jupyter notebook dengan path direktori folder project tersebut
7. Untuk mengganti jumlah finetuning layer, pada bagian markdown "Memuat Layer" ubah angkanya sesuai yang diinginkan
```python
# Freeze the layers of the pre-trained model
pretrained_model.trainable = True

# Optionally, freeze the first few layers
for layer in pretrained_model.layers[:-30]:  # <= ubah disini
    layer.trainable = False
```

8. ika ingin tanpa finetuning, pada pada bagian markdown "Memuat Layer" ubah kodenya menjadi berikut
```python
pretrained_model.trainable = False
```

9. Jalankan program 

## 📌 Catatan
* Proyek ini ditujukan untuk pembelajaran dalam bidang computer vision, khususnya dalam konteks makanan tradisional Indonesia.

* Model ini dapat diadaptasi untuk jenis klasifikasi citra lainnya dengan mengganti dataset dan melakukan fine-tuning sesuai kebutuhan.
