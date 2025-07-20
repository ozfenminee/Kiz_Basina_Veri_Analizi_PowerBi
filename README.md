# Power BI ile Veri Analizi ve Görselleştirme

Bu proje, katılımcıların kendi seçtiği veri seti üzerinden Power BI kullanarak analiz ve görselleştirme sürecini uyguladığı bir çalışmadır.

## Proje Amacı

- Sayısal ve kategorik değişkenler üzerinde veri temizleme
- Dönüştürme işlemleri (veri tipi, boşluk temizliği, etiket düzeltme)
- DAX sorguları ile hesaplamalar (örnek: toplam, ortalama, oran)
- Power BI ile etkili görselleştirmeler üretmek

##  Kullanılan Teknolojiler

- Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)

## Uygulama Adımları

1. Veri seti içe aktarıldı (Excel/CSV)
2. Power Query ile veri temizleme ve dönüştürme işlemleri yapıldı
3. Sayısal/kategorik sütunlar ayrıştırıldı
4. DAX kullanılarak özel ölçümler tanımlandı:
   - `ToplamVaka`, `AktifVaka`, `OlumOrani` vb.
5. Bar chart, pie chart, card gibi görsellerle interaktif bir rapor oluşturuldu

##  Örnek DAX Ölçüleri

```dax
ToplamVaka = SUM(Confirmed)
AktifVaka = SUM(Confirmed) - SUM(Recovered) - SUM(Deaths)
OlumOrani = DIVIDE(SUM(Deaths), SUM(Confirmed), 0)
