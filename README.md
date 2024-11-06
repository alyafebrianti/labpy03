## LATIHAN 1 
```python
import random

# Meminta pengguna memasukkan nilai n
n = int(input("Masukkan nilai N: "))

# Looping untuk menghasilkan n bilangan acak
for i in range(1, n + 1):
    # Menghasilkan bilangan acak antara 1 dan 5
    bilangan_acak = random.uniform(1, 5)

    # Menampilkan data ke-i dan nilai bilangan acak
    print(f"data ke: {i} => {bilangan_acak}")
    print("Selesai")
```
## Output 
````markdown
Masukkan nilai N: 5
data ke: 1 => 4.008043893980016
Selesai
data ke: 2 => 2.8564336901188367
Selesai
data ke: 3 => 4.3889920192245055
Selesai
data ke: 4 => 1.2014110051103857
Selesai
data ke: 5 => 1.442726420829001
Selesai
````

## Penjelasan latihan 1
1. Posisi "Selesai": Kata "Selesai" dicetak setelah setiap bilangan acak. Jika Anda ingin kata "Selesai" hanya dicetak setelah seluruh loop selesai, maka sebaiknya letakkan di luar loop.
2. Indentasi dalam loop: Indentasi dan strukturnya sudah benar, jadi Anda tidak perlu khawatir tentang itu.
Berikut adalah penjelasan lengkap mengenai kode Python yang Anda berikan:

### Kode:
```python
import random

# Meminta pengguna memasukkan nilai n
n = int(input("Masukkan nilai N: "))

# Looping untuk menghasilkan n bilangan acak
for i in range(1, n + 1):
    # Menghasilkan bilangan acak antara 1 dan 5
    bilangan_acak = random.uniform(1, 5)

    # Menampilkan data ke-i dan nilai bilangan acak
    print(f"data ke: {i} => {bilangan_acak}")
    print("Selesai")
```

### Penjelasan Langkah demi Langkah:

1. Import Modul `random`:
   ```python
   import random
   ```
   Di bagian ini, Anda mengimpor modul `random`, yang memungkinkan Anda untuk menghasilkan bilangan acak. Fungsi `random.uniform()` digunakan untuk menghasilkan bilangan acak float dalam rentang tertentu.

2. Meminta Input dari Pengguna:
   ```python
   n = int(input("Masukkan nilai N: "))
   ```
   Kode ini meminta pengguna untuk memasukkan sebuah nilai integer yang disebut `n`. Nilai `n` ini akan menentukan berapa kali loop `for` akan dijalankan. Fungsi `input()` mengambil input dari pengguna dalam bentuk string, dan kemudian fungsi `int()` mengubahnya menjadi tipe data integer.

3. Looping untuk Menghasilkan Bilangan Acak:
   ```python
   for i in range(1, n + 1):
   ```
   Di sini, loop `for` akan dimulai dari `i = 1` dan berjalan hingga `i = n`. Fungsi `range(1, n + 1)` menghasilkan urutan angka mulai dari 1 hingga `n`. Jadi, jika pengguna memasukkan `n = 5`, loop ini akan dijalankan 5 kali, dengan nilai `i` yang bervariasi dari 1 hingga 5.

4. Menghasilkan Bilangan Acak:
   ```python
   bilangan_acak = random.uniform(1, 5)
   ```
   Setiap kali loop dijalankan, kode ini menghasilkan sebuah bilangan acak float di antara 1 dan 5. Fungsi `random.uniform(1, 5)` menghasilkan nilai acak dengan batas bawah 1 dan batas atas 5 (termasuk desimal). Hasilnya disimpan dalam variabel `bilangan_acak`.

5. Menampilkan Hasil:
   ```python
   print(f"data ke: {i} => {bilangan_acak}")
   ```
   Di bagian ini, program menampilkan hasil bilangan acak yang telah dihasilkan. Dengan menggunakan f-string, nilai dari `i` (nomor urut data) dan `bilangan_acak` akan dicetak dalam format yang rapi, seperti "data ke: 1 => 3.12" jika nilai `i` adalah 1 dan `bilangan_acak` adalah 3.12.

6. Mencetak Kata "Selesai" Setiap Kali dalam Loop:
   ```python
   print("Selesai")
   ```
   Setelah mencetak hasil untuk setiap bilangan acak, perintah ini mencetak kata "Selesai". Karena perintah ini berada di dalam loop, kata "Selesai" akan dicetak setelah setiap iterasi (setiap kali bilangan acak dicetak).

## Penjelasan Output
Untuk setiap iterasi dari loop:
1. Program mencetak bilangan acak untuk `data ke-1`, `data ke-2`, dan seterusnya.
2. Setelah itu, kata "Selesai"dicetak. 
- Kata "Selesai" akan dicetak setelah setiap bilangan acak. Jika Anda hanya ingin kata "Selesai" muncul sekali di akhir setelah seluruh loop selesai, Anda harus memindahkan `print("Selesai")` ke luar loop.

## LATIHAN 2
```python
# Inisialisasi laba per bulan
laba = 0
total_laba = 0

# Loop untuk bulan 1 sampai 8
for bulan in range(1, 9):
    # Menentukan laba berdasarkan bulan
    if bulan in [1, 2]:  # Bulan 1 dan 2
        laba = 0
    elif bulan in [3, 4]:  # Bulan 3 dan 4
        laba = 10000000.0
    elif bulan in [5, 6, 7]:  # Bulan 5, 6, dan 7
        laba = 50000000.0
    elif bulan == 8:  # Bulan 8
        laba = 200000000.0
    
    # Menampilkan laba per bulan
    print(f"laba bulan ke- {bulan} sebesar: {laba}")
    
    # Menambahkan laba ke total laba
    total_laba += laba

# Menampilkan total laba
print(f"Total laba adalah: {total_laba}")
```

## Output
````markdown
laba bulan ke- 1 sebesar: 0
laba bulan ke- 2 sebesar: 0
laba bulan ke- 3 sebesar: 10000000.0
laba bulan ke- 4 sebesar: 10000000.0
laba bulan ke- 5 sebesar: 50000000.0
laba bulan ke- 6 sebesar: 50000000.0
laba bulan ke- 7 sebesar: 50000000.0
laba bulan ke- 8 sebesar: 200000000.0
Total laba adalah: 370000000.0
````

## LATIHAN 3
```python
def atm():
  saldo = 10000000000

  while True:
    print("Saldo saat ini: Rp", saldo)
    print("1. Tarik Uang")
    print("2. Keluar")
    pilihan = int(input("Pilih menu (1/2): "))

    if pilihan == 1:
      jumlah_tarik = int(input("Masukkan jumlah penarikan: "))
      if jumlah_tarik <= saldo:
        saldo -= jumlah_tarik
        print("Penarikan berhasil!")
      else:
        print("Saldo tidak mencukupi!")
    elif pilihan == 2:
      print("Terima kasih telah menggunakan ATM!")
      break
    else:
      print("Pilihan tidak valid!")

atm()
```

## Output
````markdown
Saldo saat ini: Rp 10000000000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan jumlah penarikan: 10000000000
Penarikan berhasil!
Saldo saat ini: Rp 0
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 2
Terima kasih telah menggunakan ATM!
````


