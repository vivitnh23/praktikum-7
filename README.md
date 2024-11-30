# praktikum-7
# Vivit Nurul Hidayah
# kelas : TI.24.A1

## Deskripsi program Program Manajemen Data Mahasiswa
Program Python sederhana untuk mengelola data mahasiswa beserta nilai mereka. Program ini memiliki fitur untuk menambah, menampilkan, mengubah, dan menghapus data mahasiswa melalui menu interaktif berbasis teks.

## Fitur Program 
- Tambah Data: Menambahkan data mahasiswa baru dengan nama dan nilai.
- Tampilkan Data: Menampilkan daftar seluruh mahasiswa beserta nilainya.
- Hapus Data: Menghapus data mahasiswa berdasarkan nama.
- Ubah Data: Mengubah nilai mahasiswa yang sudah terdaftar.
- Keluar: Mengakhiri program.

  ## Flowchart
  ![Flowchart](https://github.com/vivitnh23/praktikum-7/blob/main/flowchar.drawio.png?raw=true)

  ## Kode Program
  ```python
	mahasiswa = {}
	def tambah(nama, nilai):
    mahasiswa[nama] = nilai
    print(f"Data mahasiswa {nama} dengan nilai {nilai} telah ditambahkan.")
    
	def tampilkan():
    if mahasiswa:
        print("Daftar Mahasiswa dan Nilai:")
        for nama, nilai in mahasiswa.items():
            print(f"Nama: {nama}, Nilai: {nilai}")
    else:
        print("Tidak ada data mahasiswa.")

	def hapus(nama):
    if nama in mahasiswa:
        del mahasiswa[nama]
        print(f"Data mahasiswa {nama} telah dihapus.")
    else:
        print(f"Mahasiswa dengan nama {nama} tidak ditemukan.")

	def ubah(nama, nilai_baru):
    if nama in mahasiswa:
        mahasiswa[nama] = nilai_baru
        print(f"Data mahasiswa {nama} telah diubah menjadi nilai {nilai_baru}.")
    else:
        print(f"Mahasiswa dengan nama {nama} tidak ditemukan.")

	def menu():
    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")
        pilihan = input("Pilih menu (1/2/3/4/5): ")

        if pilihan == '1':
            nama = input("Masukkan nama mahasiswa: ")
            nilai = input("Masukkan nilai mahasiswa: ")
            tambah(nama, nilai)
        elif pilihan == '2':
            tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            nilai_baru = input("Masukkan nilai baru: ")
            ubah(nama, nilai_baru)
        elif pilihan == '5':
            print("Keluar dari program.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

  	menu()
  ```

## Output Program
````

Menu:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Pilih menu (1/2/3/4/5): 1
Masukkan nama mahasiswa: vivit nurul hidayah
Masukkan nilai mahasiswa: 98
Data mahasiswa vivit nurul hidayah dengan nilai 98 telah ditambahkan.

Menu:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Pilih menu (1/2/3/4/5): 1
Masukkan nama mahasiswa: jeon jungkook 
Masukkan nilai mahasiswa: 90
Data mahasiswa jeon jungkook  dengan nilai 90 telah ditambahkan.

Menu:
1. Tambah Data
2. Tampilkan Data
3. Hapus Data
4. Ubah Data
5. Keluar
Pilih menu (1/2/3/4/5): 2
Daftar Mahasiswa dan Nilai:
Nama: vivit nurul hidayah, Nilai: 98
Nama: jeon jungkook , Nilai: 90

````
# Cara Kerja Program
- Mulai Program: Program menampilkan menu utama dengan 5 opsi.
- Pilih Opsi: Pengguna memilih salah satu dari:
- Tambah Data: Memasukkan nama dan nilai mahasiswa ke dalam database.
- Tampilkan Data: Menampilkan daftar mahasiswa atau pesan jika kosong.
- Hapus Data: Menghapus data mahasiswa berdasarkan nama.
- Ubah Data: Mengubah nilai mahasiswa berdasarkan nama.
- Keluar: Mengakhiri program.
- Eksekusi Pilihan: Program menjalankan perintah sesuai opsi yang dipilih.
- Ulangi atau Keluar: Program kembali ke menu hingga pengguna memilih keluar.

  
  
