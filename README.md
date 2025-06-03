# manajemen-daftar-belanja
Aplikasi Python sederhana untuk mengelola daftar belanja menggunakan struktur data list. Dibuat untuk tugas mata kuliah Pengantar Pemrograman.
print("Hello, World!")

# Menampilkan Menu Daftar Belanja
def tampilkan_menu():
    print("\n=== Menu Daftar Belanja ===")
    print("1. Tambah barang")
    print("2. Hapus barang")
    print("3. Lihat daftar belanja")
    print("4. Urutkan daftar")
    print("5. Lihat jumlah item")
    print("6. Cari barang")
    print("7. Keluar")

# Fungsi untuk menambah barang
def tambah_barang(daftar):
    barang = input("Masukkan nama barang: ")
    daftar.append(barang)
    print(f"{barang} berhasil ditambahkan.")

# Fungsi untuk menghapus barang
def hapus_barang(daftar):
    barang = input("Masukkan nama barang yang ingin dihapus: ")
    if barang in daftar:
        daftar.remove(barang)
        print(f"{barang} berhasil dihapus.")
    else:
        print(f"{barang} tidak ditemukan dalam daftar.")

# Fungsi untuk melihat daftar
def lihat_daftar(daftar):
    if not daftar:
        print("Daftar belanja kosong.")
    else:
        print("\n--- Daftar Belanja ---")
        for i, item in enumerate(daftar, 1):
            print(f"{i}. {item}")

# Fungsi untuk mengurutkan daftar
def urutkan_daftar(daftar):
    daftar.sort()
    print("Daftar berhasil diurutkan.")

# Fungsi untuk menghitung jumlah item
def jumlah_item(daftar):
    print(f"Jumlah total item: {len(daftar)}")

# Fungsi untuk mencari barang
def cari_barang(daftar):
    barang = input("Masukkan nama barang yang ingin dicari: ")
    if barang in daftar:
        print(f"{barang} ditemukan dalam daftar.")
    else:
        print(f"{barang} tidak ditemukan.")

# Program utama
def main():
    daftar_belanja = []
    
    while True:
        tampilkan_menu()
        pilihan = input("Pilih menu (1-7): ")

        if pilihan == "1":
            tambah_barang(daftar_belanja)
        elif pilihan == "2":
            hapus_barang(daftar_belanja)
        elif pilihan == "3":
            lihat_daftar(daftar_belanja)
        elif pilihan == "4":
            urutkan_daftar(daftar_belanja)
        elif pilihan == "5":
            jumlah_item(daftar_belanja)
        elif pilihan == "6":
            cari_barang(daftar_belanja)
        elif pilihan == "7":
            print("Terima kasih! Program selesai.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

# Jalankan program
if __name__ == "__main__":
    main() 
