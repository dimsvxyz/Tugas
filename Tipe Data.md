Di NumPy, dtype bukan sekadar label namun sebuah objek metadata yang memberi tahu sistem komputer secara spesifik bagaimana cara menginterpretasikan dan mengelola byte data di dalam array (ndarray). dtype secara eksplisit mendefinisikan ukuran memori (dalam bit) yang harus dialokasikan untuk setiap elemen dalam array (misalnya, int32 berarti 4 byte per elemen). Semua elemen dalam satu ndarray diwajibkan memiliki dtype yang sama. 

## Tipe Data

'''A. Integer (Bilangan Bulat)
NumPy membagi integer menjadi tipe bertanda (signed) (dapat menyimpan positif dan negatif) dan tak bertanda (unsigned) (hanya positif). 

np.int64	64-bit	Rentang nilai yang sangat besar	Tipe default untuk integer, menjamin keamanan data.
np.int32	32-bit	Rentang nilai hingga ≈2 Miliar	Hemat memori, cocok jika rentang nilai data sudah terjamin.
np.uint8	8-bit	0 hingga 255	Penting untuk image processing, di mana setiap piksel diwakili oleh 1 byte. 

B. Floating Point (Bilangan Desimal)
Tipe float penting untuk  menangani angka desimal.

np.float64	64-bit	Presisi Ganda (Double Precision)	Tipe default float, digunakan ketika presisi perhitungan sangat penting (misalnya, fisika, keuangan).
np.float32	32-bit	Presisi Tunggal (Single Precision)	Digunakan secara luas dalam deep learning dan grafika komputer untuk meningkatkan kecepatan komputasi dan mengurangi kebutuhan memori GPU.
np.float16	16-bit	Presisi Setengah	Digunakan dalam Machine Learning tingkat lanjut (misalnya, model Transformer) untuk efisiensi memori yang ekstrem.```

C. Non Numerik
1. np.bool_ (Boolean)
Representasi logika (True atau False).
Tipe ini hanya menyimpan salah satu dari dua nilai: True (diwakili sebagai 1) atau False (diwakili sebagai 0). Meskipun hanya 1 byte, ini adalah tipe yang paling efisien untuk logika.Dimana array digunakan sebagai filter untuk memilih elemen tertentu dari array lain yang memenuhi kondisi True. Digunakan untuk membuat masker yang memilih semua data yang lebih besar dari suatu nilai tertentu.

2. np.datetime64 (Tanggal dan Waktu)
Analisis Deret Waktu (Time Series), perhitungan perbedaan waktu.
NumPy menyediakan datetime64 untuk representasi data tanggal dan waktu secara presisi dan efisien, jauh lebih baik daripada objek datetime Python standar untuk operasi array skala besar. Tipe ini memungkinkan kita melakukan aritmatika waktu yang mudah (misalnya, mengurangi dua tanggal untuk mendapatkan durasi) dan menentukan resolusi waktu (seperti hari, jam, atau nanodetik), misalnya: datetime64[D] untuk presisi hari.

3. 'U' + ukuran (Unicode String)
Menyimpan data teks.
Tidak seperti string Python yang ukurannya dinamis, NumPy menggunakan string berukuran tetap. Tipe ini dideklarasikan dengan format 'U' (Unicode) diikuti oleh angka yang menunjukkan panjang maksimum string (misalnya, 'U10' berarti string maksimum 10 karakter). Kekurangan utama tipe ini adalah jika string melebihi ukuran yang ditentukan, maka string akan terpotong. Digunakan untuk menyimpan label kategori atau nama kolom, di mana panjang teks biasanya sudah diketahui atau terbatas.


```import numpy as np

int_array = np.array([ , , , ], dtype=np.int32)
print("Integer Array:", int_array, "dtype:", int_array.dtype)

float_array = np.array([ , , , ], dtype=np.float64)
print("Floating Point Array:", float_array, "dtype:", float_array.dtype)

uint_array = np.array([ , , , ], dtype=np.uint8)
print("Unsigned Int Array:", uint_array, "dtype:", uint_array.dtype)

complex_array = np.array([ , , , ], dtype=np.complex64)
print("Complex Array:", complex_array, "dtype:", complex_array.dtype)

bool_array = np.array([ , , , ], dtype=np.bool_)
print("Boolean Array:", bool_array,"dtype:", bool_array.dtype)

datetime_array = np.array([ , , , ], dtype='datetime64[D]')
print("Datetime Array:", datetime_array, "dtype:", datetime_array.dtype)

string_array = np.array(["Halo", "NumPy", "DataScience", "Kece"], dtype='<U...')
print("Unicode String Array:", string_array, "dtype:", string_array.dtype)


