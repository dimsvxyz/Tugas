Sebuah data memiliki tipe yang berbeda-beda. Dalam Python, tipe data ini saya kelompokkan menjadi dua kategori utama: Tipe Data Primitif dan Tipe Data Koleksi 


Tipe Data Primitif
Tipe data primitif adalah jenis data yang paling dasar dalam pemrograman. Tipe data ini hanya menyimpan satu nilai (single value) saja.

1. Numbers (Angka)
Tipe data untuk nilai-nilai angka.

Integer (int): Bilangan bulat, baik positif maupun negatif, dan tidak memiliki angka desimal.

Contoh: 1, -18, 666, dan 0.

Float (float): Bilangan riil yang bisa mewakili bilangan bulat atau bilangan desimal (memiliki titik).

Contoh: 3.14, 1.0 (walaupun bulat, ia ditandai sebagai float).

Complex (complex): Bilangan kompleks. (Tipe ini tidak akan kita gunakan di kelas ini, tapi perlu diketahui.)

Contoh: 1+2j.

2. Boolean (bool)
Boolean merupakan tipe data yang sangat penting karena hanya bernilai True (Benar) atau False (Salah). Tipe data ini merepresentasikan nilai kebenaran (truth values) dan dipakai dalam logika program (kondisi if/else).

Contoh:

Python

print(10 > 5)  # Hasilnya: True
print(10 == 5) # Hasilnya: False

Nilai yang Dianggap False (Falsy Values)
Sebenarnya, hampir semua variabel yang memiliki nilai bisa dievaluasi dan menghasilkan nilai True. Hanya ada beberapa nilai yang secara default akan dianggap bernilai False, yaitu:

Nilai yang sudah didefinisikan salah: None dan False.

Angka nol dari semua tipe numerik: 0, 0.0, 0j.

Urutan (sequence) dan koleksi (collection) yang kosong: "" (string kosong), () (tuple kosong), {} (dictionary kosong), set() (set kosong), range(0).

3. String (str)
String merupakan urutan karakter (huruf, angka, simbol) yang digunakan untuk data teks. Ketika saya membuat variabel bernilai string, saya harus mengapitnya dengan tanda kutip tunggal ('') atau ganda ("").

Contoh: "Apple Juice", 'Belajar Python'.



Tipe Data Koleksi (Collection)
Tipe data koleksi menyimpan satu atau lebih data primitif sebagai satu kelompok. Ini memungkinkan kita mengelola banyak data sekaligus.

1. List
List merupakan jenis kumpulan data yang terurut (ordered) dan dapat diubah (mutable). List adalah tipe data yang sangat sering saya gunakan di Python.

Inisialisasi: Menggunakan kurung siku [], dan setiap elemennya dipisahkan dengan koma.

Contoh: x = [1, 2.2, "Ea"]

Catatan Penting: Nilai dalam list selalu dimulai dari indeks ke-0. Jadi, nilai 1 pada list di atas adalah elemen pada indeks ke-0.

2. Tuple
Tuple bisa dibilang mirip dengan List, namun tidak dapat diubah (immutable) elemennya setelah dideklarasikan. Umumnya, tuple saya gunakan untuk data yang bersifat sekali deklarasi dan eksekusinya cenderung lebih cepat.

Inisialisasi: Menggunakan tanda kurung (), dan setiap elemen dipisahkan dengan koma.

Contoh: x = (1, "Black", 1+2j)

3. Set
Set merupakan kumpulan item yang bersifat unik dan tanpa urutan (unordered collection). Set otomatis akan menghilangkan elemen duplikat.

Inisialisasi: Menggunakan tanda kurawal {}, dan setiap elemen dipisahkan dengan koma.

Contoh: x = {1, 4, 9, 7, 13}

4. Dictionary (dict)
Dictionary pada Python merupakan kumpulan pasangan kunci-nilai (key-value pairs) yang bersifat tidak berurutan (meskipun terurut sejak Python 3.7). Dictionary sangat berguna untuk menyimpan data terstruktur, dari yang kecil hingga besar.

Aturan Definisi:

Setiap elemen pasangan kunci-nilai dipisahkan dengan koma (,).

Kunci dan nilai dipisahkan dengan titik dua (:).

Kunci dan nilai dapat berupa tipe variabel/objek apa pun.

Contoh:

Python

x = {
    'name': 'Duke',
    'age': 20,
    'isMarried': False
}
