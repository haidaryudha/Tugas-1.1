# Tugas-1.1

### Code
```python
    if berat > 5:  # Jika berat lebih dari 5 kg
        biaya += 5000  # Tambah biaya 5000

    if jarak > 10:  # Jika jarak lebih dari 10 km
        biaya += 8000  # Tambah biaya 8000

    if express:  # Jika pengiriman express (True)
        biaya += 20000  # Tambah biaya 20000

    if member:  # Jika pengguna adalah member (True)
        biaya *= 0.9  # Berikan diskon 10% (biaya dikali 0.9)

    return int(biaya)  # Pastikan biaya dikembalikan sebagai bilangan bulat
```

### Inisialisasi Biaya Dasar
Pada awalnya, fungsi menetapkan biaya dasar pengiriman sebesar **10.000** rupiah:  
```python
biaya = 10000
```
Jadi, sebelum ada perhitungan tambahan, biaya pengiriman dimulai dari angka ini.  

---

### Menentukan Biaya Tambahan Berdasarkan Berat
Setelah biaya dasar ditetapkan, program akan mengecek apakah berat barang lebih dari **5 kg**. Jika iya, biaya akan ditambah sebesar **5.000** rupiah:  
```python
if berat > 5:
    biaya += 5000
```
Pada contoh yang diberikan, berat barang adalah **6 kg**, yang berarti lebih dari **5 kg**. Oleh karena itu, biaya tambahan sebesar **5.000** ditambahkan ke biaya awal.  
**Total biaya saat ini: 10.000 + 5.000 = 15.000 rupiah.**  

---

###  Menentukan Biaya Tambahan Berdasarkan Jarak
Selanjutnya, program akan mengecek apakah jarak pengiriman lebih dari **10 km**. Jika iya, maka biaya akan bertambah sebesar **8.000** rupiah:  
```python
if jarak > 10:
    biaya += 8000
```
Pada contoh ini, jarak pengiriman adalah **15 km**, yang lebih besar dari **10 km**, sehingga biaya tambahan sebesar **8.000** rupiah diterapkan.  
**Total biaya sekarang: 15.000 + 8.000 = 23.000 rupiah.**  

---

### Menentukan Biaya Tambahan untuk Pengiriman Express 
Jika pengguna memilih pengiriman express, biaya tambahan sebesar **20.000** rupiah akan ditambahkan:  
```python
if express:
    biaya += 20000
```
Dalam contoh ini, parameter `express=True`, yang berarti pengguna memilih layanan pengiriman express. Oleh karena itu, biaya tambahan **20.000** ditambahkan ke total biaya sebelumnya.  
**Total biaya sekarang: 23.000 + 20.000 = 43.000 rupiah.**  

---

###  Memberikan Diskon Jika Pengguna adalah Member
Jika pengguna adalah anggota (member), maka biaya akhir akan dikalikan dengan **0.9** untuk memberikan diskon sebesar **10%**:  
```python
if member:
    biaya *= 0.9
```
Karena `member=True` dalam contoh ini, biaya saat ini yaitu **43.000** akan dikalikan dengan **0.9**, sehingga:  
**43.000 × 0.9 = 38.700 rupiah.**  

---

### Mengembalikan Nilai Biaya sebagai Bilangan Bulat
Karena perhitungan diskon bisa menghasilkan angka desimal, fungsi memastikan bahwa hasil akhirnya dikonversi menjadi bilangan bulat (`int`), agar hasilnya tidak memiliki koma atau pecahan:  
```python
return int(biaya)
```
Sehingga, meskipun hasil perhitungan diskon adalah **38.700**, program akan mengembalikan **38.700** sebagai integer (bilangan bulat).  

---

###  Memanggil Fungsi dan Menampilkan Hasil
Pada baris terakhir dari kode:  
```python
print(hitung_biaya_pengiriman(6, 15, express=True, member=True))
```
Fungsi `hitung_biaya_pengiriman()` dipanggil dengan parameter **6 kg**, **15 km**, **express=True**, dan **member=True**.  
Hasil akhirnya adalah **38.700**, yang kemudian dicetak ke layar sebagai output.  
