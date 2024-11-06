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

     
    
