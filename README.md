# Biodata
Nama: Marsya Nabila Putri

Kelas: TI.24.A.4

NIM: 312410338

Matkul: Pemrograman

# TUGAS PRATIKUM
![FOTO](https://github.com/user-attachments/assets/3f2f2291-a41d-48ff-b3db-99366eacf56b)

# Laboratorium 8.py
```python
class Mahasiswa:
    def _init_(self, nama, nilai):
        self.nama = nama
        self.nilai = nilai

class DaftarNilaiMahasiswa:
    def _init_(self):
        self.daftar_nilai = {}

    def tambah(self, nama, nilai):
        """Menambahkan data mahasiswa"""
        self.daftar_nilai[nama] = Mahasiswa(nama, nilai)
        print(f"Data {nama} berhasil ditambahkan.")

    def tampilkan(self):
        """Menampilkan data mahasiswa"""
        print("Daftar Nilai Mahasiswa:")
        for mahasiswa in self.daftar_nilai.values():
            print(f"Nama: {mahasiswa.nama}, Nilai: {mahasiswa.nilai}")

    def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama"""
        if nama in self.daftar_nilai:
            del self.daftar_nilai[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def ubah(self, nama, nilai_baru):
        """Mengubah data mahasiswa berdasarkan nama"""
        if nama in self.daftar_nilai:
            self.daftar_nilai[nama].nilai = nilai_baru
            print(f"Data {nama} berhasil diubah.")
        else:
            print(f"Data {nama} tidak ditemukan.")
            
daftar_nilai = DaftarNilaiMahasiswa()

while True:
    print("\nMenu:")
    print("1. Tambah Data")
    print("2. Tampilkan Data")
    print("3. Hapus Data")
    print("4. Ubah Data")
    print("5. Keluar")

    pilihan = input("Pilih menu: ")

    if pilihan == "1":
        nama = input("Masukkan nama: ")
        nilai = input("Masukkan nilai: ")
        daftar_nilai.tambah(nama, nilai)
    elif pilihan == "2":
        daftar_nilai.tampilkan()
    elif pilihan == "3":
        nama = input("Masukkan nama: ")
        daftar_nilai.hapus(nama)
    elif pilihan == "4":
        nama = input("Masukkan nama: ")
        nilai_baru = input("Masukkan nilai baru: ")
        daftar_nilai.ubah(nama, nilai_baru)
    elif pilihan == "5":
        break
    else:
        print("Pilihan tidak valid.")
````

# Penjelasan Kode 
1. `Daftar Nilai Mahasiswa` adalah kelas yang mengelola daftar siswa. Kelas ini memiliki metode untuk menambah, mengubah, menghapus, dan menampilkan daftar nilai siswa.
2. Metode `tambah(self, nama, nilai)` Menambahkan data siswa baru ke dalam daftar.
3. Metode `tampilkan(self)` Menampilkan semua data siswa yang tersimpan dalam daftar.
4. Metode `hapus(self, nama)` Menghapus data siswa berdasarkan nama.
5. Metode `ubah(self, nama, nilai_baru)` Mengubah nilai siswa yang sudah ada berdasarkan nama.
6. Metode `daftar_nilai` menampilkan daftar nilai semua siswa

Mencetak menu dengan lima opsi yang dapat dipilih pengguna tersebut:

1. Tambah data: untuk menambahkan data siswa baru
2. Tampilkan data: untuk menampilkan semua data siswa yang telah dimasukkan
3. Hapus data: Menghapus data siswa berdasarkan nama
4. Ubah data: Mengubah nilai siswa berdasarkan nama
5. Keluar: Keluar dari program

Kelas Diagram:

![draw](https://github.com/user-attachments/assets/bcd9b482-5c89-4071-b269-a0cc8382b247)

Flowchart:

![flowchart8](https://github.com/user-attachments/assets/870ef50a-de46-4ff7-a714-056e1fc10e39)




