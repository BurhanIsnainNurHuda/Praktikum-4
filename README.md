# Praktikum-4

# Tugas Praktikum 
Buat program sederhana untuk menambahkan data kedalam sebuah list dengan rincian sebagai berikut:
  
   • Progam meminta memasukkan data sebanyak-banyaknya (gunakan perulangan) 
  
   • Tampilkan pertanyaan untuk menambah data (y/t?), apabila jawaban t (Tidak), maka program akan menampilkan daftar datanya.
  
   • Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%,
uts: 35%, uas: 35%)
   
   • Buat flowchart dan penjelasan program 

 # Penjelasan Program

 1. Import dan Definisi Fungsi
 
        def hitung_nilai_akhir(nilai_tugas, nilai_uts, nilai_uas):
        # Menghitung nilai akhir berdasarkan persentase
        return (nilai_tugas * 0.30) + (nilai_uts * 0.35) + (nilai_uas * 0.35)

  • Fungsi `hitung_nilai_akhir`:

  • Fungsi ini menerima tiga parameter: `nilai_tugas`, `nilai_uts`, dan `nilai_uas`.

  • Fungsi ini menghitung nilai akhir dengan menggunakan rumus:
 
   • Nilai akhir = (nilai tugas * 30%) + (nilai UTS * 35%) + (nilai UAS * 35%).

 • Mengembalikan hasil perhitungan nilai akhir.


 2. Fungsi Utama

        def main():
            daftar_nilai = []

• Fungsi `main`:
 
 • Mendeklarasikan list kosong `daftar_nilai` untuk menyimpan data nilai mahasiswa.


 3. Perulangan untuk Memasukkan Data

        while True:
            # Meminta input dari pengguna
            nama = input("Masukkan nama mahasiswa: ")
            nilai_tugas = float(input("Masukkan nilai tugas: "))
            nilai_uts = float(input("Masukkan nilai UTS: "))
            nilai_uas = float(input("Masukkan nilai UAS: "))

• Perulangan `while True`:

• Memungkinkan pengguna untuk terus memasukkan data tanpa batasan.

• Di dalam perulangan, program meminta pengguna untuk memasukkan:
  • Nama mahasiswa
  • Nilai tugas
  • Nilai UTS
  • Nilai UAS

• Nilai tugas, UTS, dan UAS dikonversi menjadi tipe data `float` untuk memungkinkan perhitungan desimal.

  
  4. Menghitung dan Menyimpan Data

    # Menghitung nilai akhir
        nilai_akhir = hitung_nilai_akhir(nilai_tugas, nilai_uts, nilai_uas)

        # Menyimpan data ke dalam list
        daftar_nilai.append({
            'nama': nama,
            'nilai_tugas': nilai_tugas,
            'nilai_uts': nilai_uts,
            'nilai_uas': nilai_uas,
            'nilai_akhir': nilai_akhir
        })

• Menghitung nilai akhir:
  
   • Memanggil fungsi `hitung_nilai_akhir` dengan nilai yang dimasukkan untuk mendapatkan nilai akhir.

• Menyimpan data:
   
   • Menambahkan dictionary ke dalam list `daftar_nilai`. Dictionary ini berisi:
 • Nama mahasiswa
 • Nilai tugas
 • Nilai UTS
 • Nilai UAS
 • Nilai akhir


  5. Menanyakan Apakah Ingin Menambah Data

• Program menanyakan kepada pengguna apakah mereka ingin menambah data lagi dengan pertanyaan "Apakah Anda ingin menambah data? (y/t)".

• Input dari pengguna diubah menjadi huruf kecil dengan `.lower()` untuk memastikan perbandingan yang konsisten.

• Jika pengguna menjawab 't' (tidak), perulangan akan dihentikan dengan `break`.

  
  6. Menampilkan Daftar Nilai

• Setelah perulangan berhenti, program mencetak "Daftar Nilai Mahasiswa:".

• Menggunakan perulangan `for`, program iterates melalui setiap item dalam `daftar_nilai` dan mencetak informasi mahasiswa dengan format yang rapi.

• Nilai akhir ditampilkan dengan dua angka desimal menggunakan format `:.2f`.

  
  7. Menjalankan Program

• Bagian ini memastikan bahwa fungsi `main()` hanya akan dipanggil jika skrip dijalankan secara langsung, bukan jika diimpor sebagai modul di program lain.
