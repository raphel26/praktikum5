# praktikum5

## Nama : Raphel ajie pratama tanoyo
## Nim  :312210348
## Kelas:TI.22.A3

## Tugas Praktikum

Buat dictionary kosong
```
mahasiswa = {}
```
- Buat program untuk lihat data nya

```
def show():
    if mahasiswa.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in mahasiswa.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
            .format (a[0][: 14],a[1][0],a[1][1],a[1][2],a[1][3],a[1][4], no = i))
        print("=================================================================================")
        
    else:
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                                TIDAK ADA DATA                                 |")
        print("=================================================================================")
```

```else``` digunakan untuk menampilkan yang terjadi jika Nama yang diketik tidak ada

- Buat program untuk Tambah Data nya

```
def add():
    print("Tambah Data")
    nama = input("Nama\t : ")
    nim = input("NIM\t : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
    mahasiswa[nama] = nim, tugas, uts, uas, akhir
```

- Buat program untuk Hapus data

``` 
def delete():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")
    
    if nama in mahasiswa.keys():
        del mahasiswa[nama]
    
    else:
        print("Nama tidak ditemukan")
```

- Buat program untuk Ubah data 

```
def update():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in mahasiswa.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir

    else:
        print("Nama tidak ditemukan ")
```

- Buat program untuk Cari data

```
def search():
    print("Cari Data")
    a = input("Masukkan Nama : ")
    if a in mahasiswa.keys():
        print("===========================================================================")
        print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
        print("===========================================================================")
        print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
            .format (a , mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4] ))
        print("===========================================================================")

    else:
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                          DATA TIDAK DITEMUKAN                                 |")
        print("=================================================================================")
```
program ini berbeda dengan melihat data, program ini akan memunculkan nama yang diketik pada input


- Buat program untuk menu nya

``` 
def menu():
   

    x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
    print("\n")

    if x == 'L':
        show()
    elif x == 'T':
        add()
    elif x == 'U':
        update()
    elif x == 'H':
        delete()
    elif x == 'C':
        search()
    elif x == 'K':
        print("==========================================================================")
        print('\n')
        print("> You exit the code                        ")
        print("\n")
        print("==========================================================================")

        exit()

    else:
        print("            Kode Yang Anda Masukan Tidak Valid")
```

Program berisikan menu, jika ketik L/T/U/H/C/K maka akan menjalankan perintah program program yang diketik di atas seperti ```show()```, ```add()```, ```update()```, ```delete()```, ```search()```

- Kode nya akan berjalan dengan perintah
``` 
while True:
    menu()
```
---
#### Output nya :


- Tambah Data

![Capture1](https://user-images.githubusercontent.com/115516830/204191178-8bd33947-1af2-4ee5-9ca4-f10a307f725e.PNG)

- Lihat dengan data

![Capture 4](https://user-images.githubusercontent.com/115516830/204191829-6c5d3e7a-4c78-4305-aa28-cdd8dd2be1da.PNG)


- Ubah Data

![Capture 3](https://user-images.githubusercontent.com/115516830/204191333-c02739b5-820f-4b03-b8b5-69fca47253d8.PNG)


- Hapus Data 

![Capture 5](https://user-images.githubusercontent.com/115516830/204192163-d8a3c0b6-490a-4c97-9ec3-dda09626214d.PNG)




- Cari Data

![Capture 7](https://user-images.githubusercontent.com/115516830/204192271-bb012982-ab3e-4f58-bf47-7cb58e95f3ba.PNG)


- Keluar

![Capture 8](https://user-images.githubusercontent.com/115516830/204192340-033a55b8-503b-4d56-98fb-556b9f177010.PNG)


- Flowchart

![flowchart](https://user-images.githubusercontent.com/115516830/204192439-ee8a4b06-d25a-4ad6-9f75-e4ba50a3163f.jpg)
