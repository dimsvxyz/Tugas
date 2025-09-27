### Definisi dan Konsep Dasar (ndarray)

NumPy merupakan library esensial di Python, yang menyediakan alat fundamental untuk komputasi numerik yang cepat dan efisien. Inti dari library ini adalah objek ndarray (N-dimensional array), yang berfungsi sebagai wadah data yang lebih unggul dibandingkan list Python standar untuk data bervolume besar.Setiap elemen di dalam satu ndarray mutlak harus memiliki tipe data (dtype) yang sama. Karakteristik ini memungkinkan NumPy untuk menyimpan array dalam blok memori yang padat dan terstruktur. Ini adalah kunci utama yang membedakannya dari list Python (yang heterogen) dan merupakan sumber utama peningkatan kecepatannya. Setelah ndarray dibuat dan diinisialisasi, jumlah total elemen (ukurannya) tidak dapat diubah. umPy sebenarnya akan membuat array baru dan menyalin data lama ke struktur baru tersebut. Sifat ukuran tetap ini memastikan alokasi memori yang stabil dan efisien untuk operasi komputasi. ndarray dapat dengan mudah merepresentasikan data dalam dimensi apa pun (N-dimensional), mulai dari vektor (1 dimensi), matriks (2 dimensi), hingga tensor (3 dimensi atau lebih tinggi). Objek ndarray memungkinkan vektorisasi, yaitu kemampuan untuk menerapkan operasi matematika (seperti penjumlahan, perkalian) pada seluruh array sekaligus tanpa memerlukan perulangan (for loop) eksplisit dalam Python.

### Karakteristik data

```.ndim	(Number of Dimensions)	
Menunjukkan jumlah sumbu (axis) yang dimiliki array. Misalnya, vektor memiliki ndim=1, matriks memiliki ndim=2. Ini mendefinisikan "tingkat kedalaman" array.

.shape	(Shape of Array)	
Sebuah tuple yang menjelaskan ukuran array di setiap dimensi. Misalnya, (3, 4) berarti 3 elemen pada sumbu pertama (baris) dan 4 elemen pada sumbu kedua (kolom).

.size	(Total Number of Elements)	
Jumlah total elemen yang disimpan array. Ini adalah hasil dari perkalian semua nilai di dalam atribut .shape.

.dtype	(Data Type)	
Tipe data spesifik yang dipegang oleh setiap elemen (misalnya, int32, float64, bool_). Pemilihan dtype yang tepat sangat krusial untuk manajemen memori dan presisi.

.itemsize	(Size of One Element (Bytes))	
Menunjukkan ukuran memori yang dialokasikan untuk menyimpan satu elemen individual dalam satuan byte. Nilai ini ditentukan oleh .dtype (misalnya, float64 selalu 8 byte).

.nbytes	(Total Memory Used (Bytes))	
Menghitung total penggunaan memori oleh data array. Rumus dasarnya adalah: nbytes = size * itemsize.
```

```
import numpy as np

data = np.array([ , , , , , ,])
print("Data:", data)
print("Dimensi (ndim):", data.ndim)   
print("Shape:", data.shape)           
print("Size:", data.size)             
print("Tipe data:", data.dtype)
print("Item size  :", data.itemsize)
print("Total bytes:", data.nbytes)



