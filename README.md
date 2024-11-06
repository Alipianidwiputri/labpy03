# Modul pratikum

# Latihan 1

![Codingan 1](https://github.com/user-attachments/assets/01825fd6-f05c-43cd-b6e1-746b34c466a6)

Saya akan menjelaskan alur algoritma dari kode tersebut secara terstruktur:

1. **Inisialisasi**
   - Import fungsi random untuk menghasilkan angka acak
   - Meminta input
   - Set counter awal = 1
  
2. **Proses utama (Loop While)**
   ```
   WHILE counter <= N:
     1. Generate angka random antara 0-1
     2. IF angka random < 0.5:
     - Tampilkan "data ke-{counter} => {angka random}"
     - Tambah counter dengan 1
     3. IF angka random >=0.5:
     - Tidak melakukan apa-apa
     - Kembali ke langkah 1
      ```
   
  3. **Kondisi Terminasi**
      - Loop berhenti ketika counter > N
      - Tampilkan "Selesai"

     Flowchart algoritma:
     
     ```
     Start
        ↓
     [Input nilai N]
        ↓
     [Set counter = 1]
        ↓
     ┌─────────────────────┐
     │ While counter <= N  │←──────┐
     └─────────┬───────────┘       │
               ↓                   │
         [Generate random]         │
               ↓                   │
         [Cek random < 0.5]        │
               ↓                   │
         [Jika Ya]──→[Print data]  │
               ↓         ↓         │
       [Jika Tidak]   [counter++]  |
               │         │         │
               └─────────┘         │
                    ↑              │
                     └─────────────┘
              ↓
        [Print "Selesai"]
              ↓
             End
     ```
 **Penjelasan Detail**
 
 1. Program meminta user memasukan nilai N yang menentukan berapa banyak angka random < 0.5 yang di inginkan
    
 2. Program akan terus menghasilkan angka random sampai mendapatkan N buah angka yang nilainya < 0.5
    
          - Jika angka random ≥ 0.5: diabaikan dengan generate angka baru
          - jika angka random < 0.5: dicetak dengan counter bertambah
       
 3. Dari output yang terlihat:
          - User memasukan N = 5
          - Program menghasilkan 5 angka random < 0.5:
 ```
            data ke: 1 => 0.22422725915012398
            data ke: 2 => 0.08143383880445236
            data ke: 3 => 0.29455614142741193
            data ke: 4 => 0.12537763804880175
            data ke: 5 => 0.46041201475820446
  ```

 4. Setelah mendapatkan 5 angka yang memenuhi syarat, program selesai dan mencetak "Selesai"
    
     Program ini mendemonstrasikan konsep:
      - perulangan dengan kondisi (while loop)
      - Pengambilan keputusan (if condition)
      - pembangkitan angka random
      - Pencacahan (counter)
      - Format string untuk output
      - Saya akan menjelaskan alur algoritma dari kode perhitungan laba tersebut:

 # LATIHAN 2

 
   ![Codingan 2](https://github.com/user-attachments/assets/c1b807a4-b9e6-4c10-a589-9ffd998d6200)

1. **Inisialisasi**
   ```python
   laba_bulanan = []  # Array kosong untuk menyimpan laba per bulan
   total_laba = 0     # Variabel untuk menyimpan total laba
   modal_awal = 100000000  # Modal awal (tersirat dari output)
   ```

2. **Proses Perhitungan Laba (Loop pertama)**
   ```
   FOR bulan FROM 1 TO 8:
       1. Set laba = 0
       
       2. Hitung laba berdasarkan bulan:
          IF bulan <= 2:           # Bulan 1-2
             laba = 0
          ELSE IF bulan <= 4:      # Bulan 3-4
             laba = modal_awal * 1% (0.01)
          ELSE IF bulan <= 7:      # Bulan 5-7
             laba = modal_awal * 5% (0.05)
          ELSE:                    # Bulan 8
             laba = modal_awal * 2% (0.02)
       
       3. Simpan laba ke array laba_bulanan
       4. Tambahkan laba ke total_laba
   ```

3. **Proses Menampilkan Hasil (Loop kedua)**
   ```
   FOR bulan, laba IN laba_bulanan:
       Tampilkan "laba bulan ke-{bulan} sebesar: {laba}"
   
   Tampilkan "Total laba adalah: {total_laba}"
   ```

Flowchart algoritma:
```
        Start
          ↓
[Inisialisasi variabel]
          ↓
┌─────────────────────┐
│ For bulan 1 to 8    │
└─────────┬───────────┘
          ↓
    [Set laba = 0]
          ↓
    [Cek kondisi bulan]
          ↓
 ┌─────────────────┐
 │ Bulan 1-2: 0%   │
 │ Bulan 3-4: 1%   │
 │ Bulan 5-7: 5%   │
 │ Bulan 8: 2%     │
 └────────┬────────┘
          ↓
    [Hitung laba]
          ↓
    [Simpan ke array]
          ↓
    [Update total_laba]
          ↓
┌─────────────────────┐
│    For each laba    │
└─────────┬───────────┘
          ↓
 [Tampilkan laba per bulan]
          ↓
   [Tampilkan total laba]
          ↓
         End
```

**Output Program:**
```
laba bulan ke- 1 sebesar: 0
laba bulan ke- 2 sebesar: 0
laba bulan ke- 3 sebesar: 1000000.0
laba bulan ke- 4 sebesar: 1000000.0
laba bulan ke- 5 sebesar: 5000000.0
laba bulan ke- 6 sebesar: 5000000.0
laba bulan ke- 7 sebesar: 5000000.0
laba bulan ke- 8 sebesar: 2000000.0
Total laba adalah: 19000000.0
```

**Penjelasan Logika Bisnis:**
1. Bulan 1-2: Belum ada laba (0%)
2. Bulan 3-4: Laba 1% dari modal
3. Bulan 5-7: Laba meningkat jadi 5% dari modal
4. Bulan 8: Laba turun menjadi 2% dari modal

Program ini mendemonstrasikan konsep:
- Array dan operasi append
- Perulangan (for loop)
- Pengambilan keputusan berjenjang (if-elif-else)
- Perhitungan persentase
- Akumulasi nilai
- Format string untuk output

 # LATIHAN 3
  
![Codingan 3](https://github.com/user-attachments/assets/5855b19f-65d9-44c3-b0a0-e6b34816bcb1)

1. **Inisialisasi Program**
   ```python
   def atm_simulator():
       saldo = 1000000  # Saldo awal
   ```

2. **Alur Utama**
   ```
   LOOP Program ATM:
       1. Tampilkan menu:
          - 1. Tarik Uang
          - 2. Keluar
       
       2. Minta input pilihan menu (1/2)
       
       3. CASE Pilihan:
          CASE "1" (Tarik Uang):
             a. Minta input jumlah penarikan
             b. Validasi penarikan:
                IF jumlah > saldo:
                   Tampilkan "Maaf, saldo tidak mencukupi!"
                ELSE IF jumlah <= 0:
                   Tampilkan "Jumlah penarikan tidak valid!"
                ELSE:
                   Kurangi saldo dengan jumlah penarikan
                   Tampilkan "Penarikan berhasil!"
          
          CASE "2" (Keluar):
             a. Tampilkan "Terima kasih telah menggunakan ATM!"
             b. Keluar dari program (break)
          
          DEFAULT:
             Tampilkan "Pilihan tidak valid!"
   ```
   

Flowchart algoritma:
```
        Start
          ↓
[Inisialisasi saldo]
          ↓
┌─────────────────────┐
│ Loop ATM Program   │←─────────┐
└─────────┬───────────┘         │
          ↓                     │
    [Tampilkan Menu]            │
          ↓                     │
    [Input Pilihan]             │
          ↓                     │
    [Cek Pilihan]               │
          ↓                     │
 ┌─────────────────┐            │
 │ Pilihan = 1     │──→[Input Jumlah]    
 │ Pilihan = 2     │──→[Tampil Terima Kasih]→[Exit]
 │ Pilihan Invalid │──→[Tampil Error]
 └────────┬────────┘            │
          ↓                     │
    [Validasi Jumlah]           │
          ↓                     │
    [Update Saldo]              │
          ↓                     │
    [Tampil Status]             │
          └─────────────────────┘

```
**Output Program yang terlihat:**
```
Saldo saat ini: Rp 1000000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan jumlah penarikan: 500000
Penarikan berhasil!

Saldo saat ini: Rp 500000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 2
Terima kasih telah menggunakan ATM!
```

**Penjelasan Detail:**
1. **Struktur Data**
   - Variabel saldo: menyimpan saldo rekening
   - Variabel pilihan: menyimpan pilihan menu
   - Variabel jumlah: menyimpan jumlah penarikan

2. **Validasi**
   - Validasi pilihan menu (harus 1 atau 2)
   - Validasi jumlah penarikan:
     * Tidak boleh melebihi saldo
     * Tidak boleh negatif atau nol

3. **Fitur**
   - Cek saldo
   - Penarikan uang
   - Keluar dari program

Program ini mendemonstrasikan konsep:
- Function definition
- Loop control (break)
- Conditional statements (if-elif-else)
- Input/output handling
- Basic error handling
- Variable manipulation
- Menu-driven interface

     
    
