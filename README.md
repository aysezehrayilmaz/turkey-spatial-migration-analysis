# Spatial Analysis of Net Migration Rates in Türkiye

Bu projede Türkiye'nin 81 iline ait 2023–2024 dönemi net göç hızlarının mekânsal dağılımı incelenmiştir.

Çalışmanın amacı, net göç hızının Türkiye genelinde belirli bölgelerde kümelenme gösterip göstermediğini analiz etmek ve yükseköğretim oranı ile nüfus büyüklüğünün net göç hızı üzerindeki etkisini değerlendirmektir.

## Veri Seti

- Kaynak: TÜİK
- Dönem: 2023–2024
- Gözlem sayısı: 81 il
- Bağımlı değişken: Net göç hızı
- Bağımsız değişkenler:
  - Yükseköğretim oranı
  - Logaritmik toplam nüfus

Veri seti; illerin nüfus, aldığı göç, verdiği göç, net göç, net göç hızı ve yükseköğretim oranı bilgilerini içermektedir.

## Kullanılan Yöntemler

- Tanımlayıcı istatistikler
- Histogram ve tematik haritalar
- Quantile ve Natural Breaks haritaları
- Hinge haritası
- Queen komşuluk matrisi
- Connectivity Map
- Global Moran's I analizi
- Lokal Moran's I / LISA analizi
- OLS regresyon modeli
- Lagrange Multiplier testleri
- Spatial Autoregressive Model (SAR)
- Spatial Error Model (SEM)
- Model karşılaştırması

## Kullanılan Araçlar

- GeoDa
- Mekânsal veri analizi
- Shapefile tabanlı il sınırı verileri

## Temel Bulgular

- Global Moran's I değeri 0.096 olarak hesaplanmıştır.
- Moran's I permütasyon testi sonucunda p-değeri 0.064 bulunmuştur.
- Net göç hızında zayıf düzeyde pozitif mekânsal ilişki görülmesine rağmen, bu ilişki %5 anlamlılık düzeyinde istatistiksel olarak anlamlı değildir.
- LISA analizinde bazı illerde yerel düzeyde High-High ve Low-Low kümeleri tespit edilmiştir.
- OLS modeli net göç hızındaki değişimin yaklaşık %41.65'ini açıklamaktadır.
- Yükseköğretim oranı ve logaritmik nüfus değişkenleri net göç hızı üzerinde pozitif ve istatistiksel olarak anlamlı bulunmuştur.
- OLS modelinin artıklarında anlamlı mekânsal otokorelasyon tespit edilmemiştir.
- SAR modelindeki mekânsal gecikme katsayısı ve SEM modelindeki mekânsal hata katsayısı anlamlı bulunmamıştır.
- Model karşılaştırması sonucunda klasik OLS modelinin çalışma için yeterli olduğu değerlendirilmiştir.

## Model Karşılaştırması

| Model | Mekânsal Katsayı | R² | AIC |
|---|---:|---:|---:|
| OLS | - | 0.4165 | 594.891 |
| SAR | rho = 0.0709 | 0.4190 | 596.630 |
| SEM | lambda = -0.0306 | 0.4169 | 594.861 |

## Proje Raporu

Analizin ayrıntılı açıklamalarını, haritaları, model sonuçlarını ve yorumları aşağıdaki raporda inceleyebilirsiniz:

[Proje raporunu görüntüle](turkey-spatial-migration-analysis.pdf)

## Proje Hakkında

Bu çalışma, Uygulamalı Mekânsal İstatistik dersi kapsamında hazırlanmıştır. Projede Türkiye illerinin komşuluk ilişkileri dikkate alınarak net göç hızının mekânsal yapısı incelenmiş ve klasik regresyon modelleri mekânsal regresyon modelleriyle karşılaştırılmıştır.

## Hazırlayan

**Ayşe Zehra Yılmaz**  
İstatistik Bölümü Mezunu
