# Yurt Dışında Otel Açma Analizi

Kaggle'daki **Hotel Booking Demand** veri seti üzerinden, yurt dışında otel açmak isteyen biri için hangi ülke pazarının daha avantajlı olabileceğini inceleyen bir veri analizi projesi. *Veri Analizinde Bilgisayar Programlama 2* dersi ödevi olarak hazırlandı.

> 📊 **Canlı raporu görüntüle:** https://oyku-kaya.github.io/otel-analizi/



## İçerik

Rapor şu soruyu yanıtlamaya çalışıyor: *"Yurt dışında bir otel açacak olsam, hangi ülke pazarına odaklanmak daha kârlı olur?"*

Bunu yapmak için şu kriterler analiz edildi:
- Ülkelere göre rezervasyon yoğunluğu (talep)
- İptal oranları (rezervasyonların ne kadarı gelire dönüşüyor?)
- Ortalama günlük gelir (ADR)
- Ortalama kalış süresi
- Otel tipinin (City vs Resort) etkisi

Raporda:
- 6 tanımsal istatistik bölümü (describe, value_counts, gruplandırma, korelasyon, vb.)
- 8 farklı görselleştirme (histogram, boxplot, bar, scatter, heatmap, gruplanmış bar)
- Her grafiğin altında kısa yorum
- 4 maddelik bulgular ve genel öneri bölümü

## Veri Seti

[Kaggle — Hotel Booking Demand Dataset](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand) — Antonio, Almeida & Nunes (2019) tarafından paylaşılan, Portekiz'deki iki otele ait yaklaşık 120 bin rezervasyon kaydı.

## Proje Yapısı

```
otel-acilis-analizi/
├── data/
│   └── hotel_bookings.csv      # Veri seti
├── notebook/
│   └── rapor.ipynb             # Çalışma dosyası
├── docs/
│   └── index.html              # Yayınlanan rapor (GitHub Pages)
├── requirements.txt
├── README.md
└── .gitignore
```

## Yerel Olarak Çalıştırmak

```bash
# 1) Sanal ortam
python -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate

# 2) Paketleri kur
pip install -r requirements.txt

# 3) Notebook'u aç
jupyter notebook notebook/rapor.ipynb
```

## HTML Raporu Yeniden Üretmek

```bash
jupyter nbconvert --to html notebook/rapor.ipynb \
    --output-dir docs --output index
```

Sonra her güncelleme için:
```bash
git add .
git commit -m "Rapor güncellendi"
git push
```

## Kullanılan Kütüphaneler

- pandas — veri işleme
- numpy — sayısal hesaplama
- matplotlib & seaborn — görselleştirme


