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
Pada kode yang Anda buat, sepertinya Anda ingin menghasilkan sejumlah bilangan acak antara 1 dan 5 sebanyak `n` kali, dan mencetak hasilnya. Namun, terdapat beberapa hal yang perlu diperbaiki untuk mencapai tujuan Anda.

1. Posisi "Selesai": Kata "Selesai" dicetak setelah setiap bilangan acak. Jika Anda ingin kata "Selesai" hanya dicetak setelah seluruh loop selesai, maka sebaiknya letakkan di luar loop.
2. Indentasi dalam loop: Indentasi dan strukturnya sudah benar, jadi Anda tidak perlu khawatir tentang itu.

Berikut adalah versi yang lebih baik dari kode Anda:

```python
import random
Meminta pengguna memasukkan nilai n
n = int(input("Masukkan nilai N: "))

# Looping untuk menghasilkan n bilangan acak
for i in range(1, n + 1):
    # Menghasilkan bilangan acak antara 1 dan 5
    bilangan_acak = random.uniform(1, 5)

    # Menampilkan data ke-i dan nilai bilangan acak
    print(f"data ke-{i} => {bilangan_acak:.2f}")  # Menampilkan bilangan dengan dua angka di belakang koma

# Menampilkan "Selesai" setelah semua bilangan acak dicetak
print("Selesai")
```

Penjelasan:
1. Fungsi `random.uniform(1, 5)`: Fungsi ini menghasilkan bilangan acak float antara 1 dan 5.
2. Format Output: Saya menambahkan format untuk membatasi output bilangan acak dengan dua angka di belakang koma (misalnya, `3.14`), agar tampilannya lebih rapi.
3. Posisi "Selesai": "Selesai" hanya dicetak setelah seluruh loop selesai untuk menghindari mencetaknya setiap kali di dalam loop.

Dengan perbaikan ini, program akan berfungsi sesuai dengan yang Anda harapkan. Semoga membantu!

## Penjelasan Output




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


