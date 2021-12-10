# TUGAS PERTEMUAN 10 DAN PENGERTIAN
## TUGAS MELENGKAPI PRAKTIKUM 10
| Nama | kelas | Nim | Matkul |
| -- | --- | ---- | ----------- |
| Heri Anto Simamora | TI.21.C.1 | 312110365 | Bahasa Perograman |

## DAFTAR ISI
| Tidak | ISI | PENJELASAN |
| -- | --- | ---------- |
| 1. | Tugas Latihan 5 | [penjelasan](#TugasLatihan) |
| 2. | Tugas Praktikum 5 | [penjelasan](#PenjelasanTugas) |

## TUGAS LATIHAN 
![gambar1](gambar/soallatihan.png.png)

## SOURCE CODE LATIHAN 
''' python

daftarKontak = {"Nama":"Nomer Telpon"}
kontak       = {'Ari':'081267888', 'Dina' : '087677776'}

print ( 30 * " " )
print ( " Nama | Nomor Telepon " ) #prinr daftarkontak 
print ( 30 * " - " )
print ( " # Ari | " , kontak [ 'Ari' ]) #print kontak Ari 
print ( " # Dina | " , kontak [ 'Dina' ]) #print kontak Dina 
print ( 30 * "═" )

#Tampilkan kontaknya Ari 
print ( "Tampilkan kontaknya Ari" )
print ( " Ari | " , kontak [ 'Ari' ]) #print kontak Ari 
print ( 30 * "═" )
#Tambah kontak baru dengan nama Riko, nomor 087654544 
print ( "Tambah kontak baru dengan nama Riko, nomor 087654544" )
kontak [ 'Riko' ] =  '087654544' 
print ( " Riko | " , kontak [ 'Riko'])
print (30 * "═" )

#Ubah kontak Dina dengan nomor baru 088999776 
print ("Ubah kontak Dina dengan nomor baru 088999776")
kontak['Dina'] =  '088999776' 
print ( " Dina | " ,kontak [ 'Dina' ])
print ( 30 * "═ " )

#Tampilkan SEMUA Nama 
print ( "Tampilkan SEMUA Nama" )
print ( kontak . keys ())
print ( 30 * "═" )

#Tampilkan semua Nomor 
print ( "Tampilkan semua Nomor" )
print ( kontak . values ())
print ( 30 * "═" )

#Tampilkan daftar Nama dan nomornya 
print ( "Tampilkan daftar Nama dan nomornya" )
print ( kontak . items ())
print ( 30 * "═" )

#MengHapus kontak Dina 
print ( "Hapus kontak Dina" )
kontak . pop ( 'Dina' )
print ( kontak . items ())
print ( 30 * "═" )

'''

## HASIL KELUARAN
![gambar2](gambar/hasilkeluaran.png.png)

## SOAL TUGAS
![gambar3](gambar/soaltugas.png.png)

## PENJELASAN TUGAS
1) Penggunaan if c.lower()<p>

if c.lower() berfungsi jika pengguna menginputkan denga huruf besar, maka otomatis akan menjadi huruf kecil sehingga kondisi yang digunakan tercapai. Contoh :<p>

jika c.lower() == 'q'<p>

2) Penggunaan while True<p>

sementara True bekerja untuk mendeteksi jika format yang diinputkan bukan berupa type maka akan muncul error<p>

3) Penggunaan lain<p>

Fungsi else jika tidak error dan tipe yang dimasukan sesuai maka proses while True<p>

4) Penggunaan valueError<p>

Fungsinya apabila diinputkan bukan berupa tipe maka hasil nya error (valueError)<p>

## SOURCE CODE TUGAS
''' python

P = print
print("Masukan data mahasiswa")
print("~~~~~~~~~~~~~~~~~~~~~~")
nama = input("Masukan Nama Anda :")
nim = int(input("Masukan NIM Anda :"))
nilai_tugas = int(input("Masukan nilai tugas :"))
nilai_uts = int(input("Masukan nilai uts :"))
nilai_uas = int(input("Masukan nilai uas :"))
while True:
    P("")
    P("")
    c = input("L)ihat, T)ambah, U)bah, H)apus, C)ari, K)eluar: ")
    if c.lower() == 'q':
       break
    elif c.lower() == 'l':
        i = open('database.txt','r').read().splitlines()
        P(" ╔═════════════════════════════════════════════════════════════════════╗")
        P(" ╠════════════════════════════ DAFTAR KONTAK ══════════════════════════╣")
        P(" ╠══════════════════╦══════════════════╦═══════╦═══════╦═══════╦═══════╣")
        P(" ║      NAMA        ║       NIM        ║ TUGAS ║  UTS  ║  UAS  ║ AKHIR ║")
        P(" ╠══════════════════╬══════════════════╬═══════╬═══════╬═══════╬═══════╣")
        for l in i:
            if l == '':
                pass
            else:
                l1 = l.replace('Nama : ','').replace('Nim : ','').replace('Tugas : ','').replace('UTS : ','').replace('UAS : ','').replace('Akhir : ','')
                na,ni,tu,uts,uas,akhir = l1.strip().split('|')
                P((' ║ ')+(na[:15]).ljust(17,'.')+('║ ')+(ni).ljust(17)+('║ ')+(tu).ljust(6)+('║ ')+(uts).ljust(6)+('║ ')+(uas).ljust(6)+('║ ')+(akhir).ljust(6)+('║'))
        P(" ╚══════════════════╩══════════════════╩═══════╩═══════╩═══════╩═══════╝")
    elif c.lower() == 'c':
        cari = input(' Mencari : ')
        i = open('database.txt','r').read().splitlines()
         P(" ╔═════════════════════════════════════════════════════════════════════╗")
        P(" ╠════════════════════════════ DAFTAR KONTAK ══════════════════════════╣")
        P(" ╠══════════════════╦══════════════════╦═══════╦═══════╦═══════╦═══════╣")
        P(" ║      NAMA        ║       NIM        ║ TUGAS ║  UTS  ║  UAS  ║ AKHIR ║")
        P(" ╠══════════════════╬══════════════════╬═══════╬═══════╬═══════╬═══════╣")
        for l in i:
            if l == '':
                pass
            elif cari in l:
                l1 = l.replace('Nama : ','').replace('Nim : ','').replace('Tugas : ','').replace('UTS : ','').replace('UAS : ','').replace('Akhir : ','')
                na,ni,tu,uts,uas,akhir = l1.strip().split('|')
                P((' ║ ')+(na).ljust(17)+('║ ')+(ni).ljust(17)+('║ ')+(tu).ljust(6)+('║ ')+(uts).ljust(6)+('║ ')+(uas).ljust(6)+('║ ')+(akhir).ljust(6)+('║'))
        P(" ╚══════════════════╩══════════════════╩═══════╩═══════╩═══════╩═══════╝")
    elif c.lower() == 'h':
        u = open('database.txt','r').read().splitlines()
        target = input(' Masukan Nama : ')
        nm = []
        for l in u:
            if l == '':
                pass
            else:
                l1 = l.replace('Nama : ','').replace('Nim : ','').replace('Tugas : ','').replace('UTS : ','').replace('UAS : ','').replace('Akhir : ','')
                na,ni,tu,uts,uas,akhir = l1.strip().split('|')
                if str(na) == str(target):
                    P('BERHASIL MENGHAPUS Data %s'%(target))
                    pass
                else:
                    nm.append(str(l)+'\n')
        new = open('database.txt','w')
        new.write(str(nm))
        new.close()
        new = open('database.txt','r').read().splitlines()
        new1 = open('database.txt','w')
        new1.close()
        new2 = open('database.txt','a')
        for i in new:
            i2 = i.replace("['","").replace("\\n', '", "\n").replace("']","").replace("\\n",'')
            new2.write(i2)
        new2.close()
    elif c.lower() == 'u':
     u = open('database.txt','r').read().splitlines()
        target = input(' Masukan Nama : ')
        nm = []
        for l in u:
            if l == '':
                pass
            else:
                l1 = l.replace('Nama : ','').replace('Nim : ','').replace('Tugas : ','').replace('UTS : ','').replace('UAS : ','').replace('Akhir : ','')
                na,ni,tu,uts,uas,akhir = l1.strip().split('|')
                if na == target:
                    P(' Mengedit Data %s'%(target))
                    while (True):
                        nama = input(" Nama : ")
                        if nama == '':
                            P(' Masukan dengan Nama Dengan Benar')
                        else:
                            break
                    while (True):
                        try:
                            nim  = int(input(" NIM  : "))
                            if nim == '':
                                P(' Masukan Nim dengan Angka')
                        except ValueError:
                            P(' Masukan Nim dengan Angka')
                        else:
                             break
                    while (True):
                        try:
                            tugas  = int(input(" TUGAS  : "))
                            if tugas == '':
                                P(' Masukan TUGAS dengan Angka')
                        except ValueError:
                            P(' Masukan TUGAS dengan Angka')
                        else:
                            break
                    while (True):
                        try:
                            uts  = int(input(" UTS  : "))
                            if uts == '':
                                P(' Masukan UTS dengan Angka')
                        except ValueError:
                            P(' Masukan UTS dengan Angka')
                        else:
                            break
                    while (True):
                        try:
                            uas  = int(input(" UAS  : "))
                             if uas == '':
                                P(' Masukan UAS dengan Angka')
                        except ValueError:
                            P(' Masukan UAS dengan Angka')
                        else:
                            break
                    akhir = round((float(tugas) * 0.3)+(float(uts) * 0.35)+(float(uas) * 0.35),2)
                    edit  =('Nama : '+nama+'|Nim : '+str(nim)+'|Tugas : '+str(tugas)+'|UTS : '+str(uts)+'|UAS : '+str(uas)+"|Akhir : "+str(akhir)+'\n')
                    nm.append(edit+'\n')
                else:
                    nm.append(str(l)+'\n')
        new = open('database.txt','w')
        new.write(str(nm))
        new.close()
        new = open('database.txt','r').read().splitlines()
        new1 = open('database.txt','w')
        new1.close()
        new2 = open('database.txt','a')
         for i in new:
            i2 = i.replace("['","").replace("\\n', '", "\n").replace("']","").replace("\\n","\n")
            new2.write(i2+'\n')
        new2.close()
    elif c.lower() == 't':
        i = open('database.txt','a')
        P(" Tambah Kontak")
        while (True):
            nama = input(" Nama : ")
            if nama == '':
                P(' Masukan dengan Nama Dengan Benar')
            else:
                break
        while (True):
            try:
                nim  = int(input(" NIM  : "))
                if nim == '':
                    P(' Masukan Nim dengan Angka')
            except ValueError:
                P(' Masukan Nim dengan Angka')
            else:
                break
        while (True):
            try:
                tugas  = int(input(" TUGAS  : "))
                if tugas == '':
                    P(' Masukan TUGAS dengan Angka')
            except ValueError:
                P(' Masukan TUGAS dengan Angka')
            else:
                break
        while (True):
            try:
                uts  = int(input(" UTS  : "))
                if uts == '':
                    P(' Masukan UTS dengan Angka')
            except ValueError:
                P(' Masukan UTS dengan Angka')
            else:
                break
        while (True):
            try:
                uas  = int(input(" UAS  : "))
                if uas == '':
                    P(' Masukan UAS dengan Angka')
            except ValueError:
                P(' Masukan UAS dengan Angka')
            else:
                break
        akhir = round((float(tugas) * 0.3)+(float(uts) * 0.35)+(float(uas) * 0.35),2)
        i.write('\nNama : '+nama+'|Nim : '+str(nim)+'|Tugas : '+str(tugas)+'|UTS : '+str(uts)+'|UAS : '+str(uas)+"|Akhir : "+str(akhir)+'\n')
        i.close()
    else:
        P("Silahkan pilih menu yang tersedia...")

'''

## HASIL OUTPUT TUGAS 

![gambar4](gambar/keluaran1.png.png)

![gambar5](gamnbar/keluaran2.png.png)

## FLOWCHART

![gambar6](gambar/flowchart.png.png)


