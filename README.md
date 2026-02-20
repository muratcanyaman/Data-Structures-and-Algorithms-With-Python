# 🧮 Python ile Veri Yapıları ve Algoritmalar

Python kullanarak **veri yapıları ve algoritmaların temellerini** pratik yaparak öğrenmek için hazırlanmış bir çalışma reposudur. Arama algoritmalarından sıralama algoritmalarına, dizilerden bağlı listelere kadar temel konuları kapsar.

---

## 📂 Proje Yapısı

```
Data-Structures-and-Algorithms-With-Python/
│
├── arrays.py                          # Dizi (Array) işlemleri
├── linear_search.py                   # Doğrusal arama algoritması
├── binary_search.py                   # İkili arama (iteratif)
├── binary_search_recursive.py         # İkili arama (rekürsif)
├── linked_list.py                     # Bağlı liste veri yapısı
├── merge_sort.py                      # Birleştirme sıralaması (dizi)
├── merge_sort_with_linked_list.py     # Birleştirme sıralaması (bağlı liste)
│
├── bogo_sort algorithm/
│   ├── bogo_sort.py                   # Bogo sıralama algoritması
│   └── unsorted_numbers.txt
│
├── merge sort recursive/
│   ├── merge_sort_recursive.py        # Rekürsif birleştirme sıralaması
│   └── unsorted_list.txt
│
├── quicksort/
│   ├── quicksort.py                   # Hızlı sıralama algoritması
│   └── unsorted_list.txt
│
└── selection sort/
    ├── selection_sort.py              # Seçmeli sıralama algoritması
    └── unsorted_list.txt
```

---

## 📖 İşlenen Konular

### 📦 Veri Yapıları

#### Diziler — `arrays.py`
- Python listesi ile dizi kullanımı
- Eleman erişimi, arama (`in` operatörü)
- Eleman ekleme: `insert()`, `append()`, `extend()`
- Eleman silme: `remove()`

#### Bağlı Liste — `linked_list.py`
- `Node` ve `LinkedList` sınıflarının tanımlanması
- Temel işlemler:

| Metot | Açıklama |
|-------|----------|
| `add(data)` | Başa yeni düğüm ekleme |
| `insert(data, index)` | Belirli bir pozisyona düğüm ekleme |
| `remove(key)` | Değere göre düğüm silme |
| `search(key)` | Listede veri arama |
| `size()` | Düğüm sayısını hesaplama |
| `is_empty()` | Listenin boş olup olmadığını kontrol etme |
| `middle_node_at_index(index)` | Belirli indexteki düğümü döndürme |

---

### 🔍 Arama Algoritmaları

#### Doğrusal Arama — `linear_search.py`
- Diziyi baştan sona tarayarak hedef elemanı bulma
- **Zaman Karmaşıklığı:** `O(n)`

#### İkili Arama (İteratif) — `binary_search.py`
- **Sıralı** bir dizide ortadan bölerek arama
- **Zaman Karmaşıklığı:** `O(log n)`

#### İkili Arama (Rekürsif) — `binary_search_recursive.py`
- İkili aramanın rekürsif versiyonu
- İteratif versiyon ile aynı zaman karmaşıklığına sahip, ancak call stack nedeniyle **daha fazla bellek** kullanır

---

### 📊 Sıralama Algoritmaları

| Algoritma | Dosya | Zaman Karmaşıklığı | Açıklama |
|-----------|-------|---------------------|----------|
| **Merge Sort** | `merge_sort.py` | `O(n log n)` | Diziyi ikiye bölüp sıralı birleştirme (dizi üzerinde) |
| **Merge Sort (Bağlı Liste)** | `merge_sort_with_linked_list.py` | `O(n log n)` | Merge sort'un bağlı liste üzerinde uygulanması |
| **Merge Sort (Rekürsif)** | `merge sort recursive/` | `O(n log n)` | Dosyadan veri okuyarak rekürsif merge sort |
| **Quick Sort** | `quicksort/` | `O(n log n)` | Pivot seçerek alt dizilere ayırma ve sıralama |
| **Selection Sort** | `selection sort/` | `O(n²)` | Her adımda en küçük elemanı bulup sıralı listeye ekleme |
| **Bogo Sort** | `bogo_sort algorithm/` | `O(n × n!)` | Rastgele karıştırarak sıralama (eğitim amaçlı) |

---

### 🔎 Algoritma Detayları

#### Merge Sort — `merge_sort.py`
- `split()`: Diziyi ortadan ikiye böler
- `merge()`: İki sıralı alt diziyi birleştirir
- `is_sorted()`: Dizinin sıralı olup olmadığını rekürsif kontrol eder

#### Merge Sort (Bağlı Liste) — `merge_sort_with_linked_list.py`
- `linked_list.py` modülünden `LinkedList` sınıfını import eder
- Bağlı listeyi ortadan bölerek (`split`) ve sıralı birleştirerek (`merge`) çalışır
- Sahte (fake) düğüm tekniği kullanılarak birleştirme işlemi gerçekleştirilir

#### Quick Sort — `quicksort/quicksort.py`
- İlk elemanı **pivot** olarak seçer
- Pivot'tan küçük ve büyük elemanları ayrı listelere ayırır
- Rekürsif olarak alt listeleri sıralayıp birleştirir

#### Selection Sort — `selection sort/selection_sort.py`
- `index_of_min()`: Sıralanmamış listede en küçük elemanın indeksini bulur
- Her adımda en küçük elemanı sıralı listeye taşır

#### Bogo Sort — `bogo_sort algorithm/bogo_sort.py`
- Listeyi rastgele karıştırarak sıralanana kadar denemeye devam eder
- Pratik kullanımı yoktur, **eğitim amaçlı** yazılmıştır

---

## 🚀 Çalıştırma

### Gereksinimler
- Python 3.6+

### Örnekleri Çalıştırma

```bash
# Diziler
python arrays.py

# Arama algoritmaları
python linear_search.py
python binary_search.py
python binary_search_recursive.py

# Bağlı liste
python linked_list.py

# Sıralama algoritmaları
python merge_sort.py
python merge_sort_with_linked_list.py

cd "merge sort recursive"
python merge_sort_recursive.py

cd quicksort
python quicksort.py

cd "selection sort"
python selection_sort.py

cd "bogo_sort algorithm"
python bogo_sort.py
```

---

## 📌 Notlar
- `unsorted_list.txt` ve `unsorted_numbers.txt` dosyaları, sıralama algoritmalarının dosyadan veri okuyarak çalışmasını göstermek için kullanılmaktadır.
- `merge_sort_with_linked_list.py` dosyası `linked_list.py` modülünü import ettiği için her iki dosyanın aynı dizinde bulunması gerekmektedir.
- Algoritmalar basitten karmaşığa doğru sıralanmıştır; sırasıyla takip etmeniz önerilir.
