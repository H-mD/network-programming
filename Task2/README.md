# Task 2

### 1. Buatlah sebuah program time server dengan ketentuan sebagai berikut

a. Membuka port di port 45000 dengan transport TCP

b. Server harus dapat melayani request yang concurrent, gunakan contoh multithreading pada ini

c. Ketentuan request yang dilayani 

- Diawali dengan string “TIME dan diakhiri dengan karakter 13 dan karakter 10”

- Setiap request dapat diakhiri dengan string “QUIT” yang diakhiri dengan karakter 13 dan 10 

d. Server akan merespon dengan jam dengan ketentuan

- Dalam bentuk string (UTF-8)
    
- Diawali dengan “JAM<spasi><jam>”
    
- <jam> berisikan info jam dalam format “hh:mm:ss” dan diakhiri dengan karakter 13 dan karakter 10

### 2. Jalankan di lab environment

a. Tuliskan dalam satu file PDF dengan nama TUGAS2.PDF

- Link menuju source code anda di github (masing-masing harus punya repository di github)

- Capturelah hasil eksekusi program server anda

## Results

![result](https://i.imgur.com/DkESZRp.png)