Dokumentasi Teknis: Aplikasi Inventori Toko Kecil
1.) Struktur File/Kode
1.	Impor Library:
-	import json:  baris pertama yang diperlukan untuk membaca dan menulis data ke format JSON.
2.	Inisialisasi Data:
-	inventory = []: list global kosong. List ini akan menyimpan semua data barang sebagai dictionary.
3.	Definisi Fungsi-fungsi: Kode-kode mendefinisikan beberapa fungsi terpisah untuk mengelola inventaris. Setiap fungsi memiliki tugas spesifiknya sendiri:
1. tambah_barang(nama, stok, harga): Untuk menambahkan item baru ke inventory.
2. tampilkan_barang(): Untuk menampilkan semua item yang ada di inventory.
3. edit_barang(index, nama=None, stok=None, harga=None): Untuk memodifikasi detail item yang sudah ada.
4. hapus_barang(index): Untuk menghapus item dari inventory.
5. laporan_ringkas(): Untuk menampilkan ringkasan total stok dan nilai inventaris.
6. simpan_ke_file(nama_file="inventori.json"): Untuk menyimpan data inventory ke dalam file JSON.
4.	Fungsi Menu Utama: menu(), berfungsi sebagai antarmuka pengguna utama yang menampilkan opsi-opsi kepada pengguna (tambah, tampilkan, edit, hapus, laporan, simpan, keluar) dan memanggil fungsi yang sesuai berdasarkan pilihan pengguna. Fungsi ini berjalan dalam sebuah loop while True agar program terus berjalan sampai pengguna memilih untuk keluar.
5.	Eksekusi Program: menu()  yang memulai program saat script Python dijalankan.

2.) Library yang Digunakan
-	JSON 
Digunakan untuk menyimpan data inventori ke dalam file inventori.json secara permanen dalam format JSON.

 
3.) Diagram Alur Kerja Aplikasi

                   [Menu Utama]


[Tambah Barang] <-> [Tampilkan Daftar]
          
      [Edit Barang]        [Hapus Barang]
        
              [Laporan Ringkas]
    
               [Simpan ke File]


4. User Manual (Ringkas)
Cara Menjalankan Aplikasi:
1. Jalankan file dengan perintah: python inventori.py
2. Ikuti menu interaktif di terminal.
Cara Tambah Data:
-	Pilih menu 1
Masukkan nama barang, stok, dan harga, Cara Edit & Hapus 
Aplikasi akan meminta:
-	Masukkan Nama Barang: (misal: Skin Care)
-	Masukkan Stok Barang: (misal: 150)
-	Masukkan Harga Barang: (misal: 310000)
Barang akan ditambahkan dan disimpan.
-	Pilih menu 3 untuk edit (masukkan nomor barang dan nilai baru)
-	Pilih menu 4 untuk hapus (masukkan nomor barang)
-	Konten File JSON : Setelah disimpan, data tersimpan dalam format: “json”
  
6. Fitur Laporan Ringkas
-	Total barang: menjumlahkan seluruh stok
-	Total nilai inventori: hasil stok × harga per barang

User Manual: Aplikasi Inventori Toko Kecil
Tujuan Aplikasi : Aplikasi ini digunakan untuk mencatat, melihat, mengedit, dan menghapus data barang pada toko kecil, serta menampilkan laporan ringkas inventori.
Cara Menjalankan Aplikasi
1.	Pastikan Python sudah terpasang di perangkat kamu.
2.	Simpan program dengan nama inventori.py.
3.	Buka terminal/command prompt.
4.	Jalankan perintah:
python inventori.py
Menu Utama
Saat dijalankan, program akan menampilkan menu seperti berikut:
=== MENU INVENTORI ===
1. Tambah Barang
2. Tampilkan Daftar Barang
3. Edit Barang
4. Hapus Barang
5. Laporan Ringkas
6. Simpan ke File
0. Keluar
Pilih menu dengan mengetik angka 0–6, lalu tekan Enter.
Fitur dan Cara Menggunakan
1. Tambah Barang
-	Pilih menu 1
-	Masukkan nama barang, jumlah stok, dan harga satuan
-	Contoh input:
Nama Barang: Skin Care
Stok: 150
Harga: 310000
2. Tampilkan Daftar Barang
-	Pilih menu 2
-	Menampilkan semua barang yang telah ditambahkan
3. Edit Barang
-	Pilih menu 3
-	Akan ditampilkan daftar barang terlebih dahulu
-	Masukkan nomor barang yang ingin diedit
-	Isi perubahan data (kosongkan jika tidak ingin diubah)
4. Hapus Barang
-	Pilih menu 4
-	Akan ditampilkan daftar barang
-	Masukkan nomor barang yang ingin dihapus
5. Laporan Ringkas
-	Pilih menu 5
-	Akan muncul total jumlah semua barang dan total nilai inventori (stok × harga)
6. Simpan ke File
-	Pilih menu 6
-	Menyimpan seluruh data ke file inventori.json dalam format JSON
0. Keluar
-	Mengakhiri aplikasi
 File Output
-	inventori.json: Berisi semua data barang dalam format yang bisa dibaca kembali atau diolah lebih lanjut.

3. Pengujian & Evaluasi (Contoh Skenario)
Berikut adalah contoh skenario pengujian yang dapat Anda lakukan:
Skenario 1: Tambah dan Hapus Barang
1.	Mulai Aplikasi: Jalankan python inventory_app.py.
2.	Tambah Barang 1:
-	Pilih 1.
-	Nama: Skin Care, Stok: 200, Harga: 330000.
-	Verifikasi pesan "Barang Skincare berhasil ditambahkan."
3.	Tampilkan Daftar Barang:
-	Pilih 1.
-	Pastikan "SkinCare" muncul dalam daftar dengan stok dan harga yang benar.
4.	Hapus Barang 1 (SkinCare):
-	Pilih 4.
-	Masukkan nomor 1 (untuk SkinCare).
-	Konfirmasi ya.
-	Verifikasi pesan "Barang Sepatu berhasil dihapus."
5.	Tampilkan Daftar Barang:
-	Pilih 2.
-	Pastikan hanya "Penghapus" yang tersisa dalam daftar.
6.	Keluar: Pilih 0.
7.	Jalankan Ulang Aplikasi: Jalankan python inventory_app.py lagi.
8.	Tampilkan Daftar Barang:
-	Pilih 2.
-	Pastikan "SkinCare" masih ada, menunjukkan data berhasil disimpan dan dimuat.

Skenario 2: Edit Barang dan Laporan
1.	Mulai Aplikasi: Jalankan python inventory_app.py. (Pastikan ada data, jika tidak, tambahkan beberapa barang terlebih dahulu).
2.	Tambah Barang (jika inventori kosong):
-	Pilih 1. Nama:SkinCare, Stok: 150, Harga:310000.
3.	Tampilkan Daftar Barang:
-	Pilih 2. Catat nomor urut untuk "SkinCare".
4.	Edit Barang "SkinCare":
-	Pilih 3. Masukkan nomor urut "1".
-	Nama Baru: (kosongkan)
-	Stok Baru: (kosongkan)
-	Harga Baru: (kosongkan)
5.	Tampilkan Daftar Barang:
Pilih 1. Pastikan "SkinCare" sekarang memiliki Stok 150 dan Harga 310000.
6.	Laporan Ringkas:
-	Pilih 5.
-	Periksa Jumlah Barang Unik, Total Stok Semua Barang, dan Total Nilai Inventori sesuai dengan data yang ada (termasuk perubahan pada "SkinCare").
7.	Keluar: Pilih 0.
