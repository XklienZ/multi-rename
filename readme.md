# multi-rename

<img src="https://github.com/XklienZ/multi-rename/blob/master/multi-rename.png" width="480" title="multi-rename">
<img src="https://github.com/XklienZ/multi-rename/blob/master/multi-rename2.png" width="480" title="multi-rename2">

Skrip ini bertujuan untuk mengganti sebagian nama file.
Secara default skrip ini untuk membantu kebutuhan pribadi saya.
Tentu Anda dapat mengganti atau mengkode ulang skrip ini untuk kebutuhan pribadi Anda.
Argumen untuk "nama baru" tidak mendukung karakter selain **[a-z] [A-Z] [0-9] . _ -**
Berhati-hati jika Anda ingin mengganti karakter spesial dalam nama file.

**CATAT:** Jalankan skrip ini di direktori defaultnya.

# OPSI
```
-t:                                                                            
    Target direktori yang ingin ditempati.                                
    Jika opsi -t di non-aktifkan, skrip akan menargetkan direktori yang sedang ditempati sekarang.
    Gunakan opsi ini di argumen pertama.
-d:
    Menghapus sebagian nama file.
    **CATAT:** Tidak dapat menghapus pada 1 nama secara keseluruhan (Menghindari nama file yang kosong).
-a:
    Targetkan file dan direktori yang tersembunyi (.).
-r:
    Targetkan semua word/kata yang cocok.
    skrip akan mengganti/menghapus word/kata yang cocok secara keseluruhan pada sebuah nama file/direktori.
```
# CARA KERJA SKRIP
    ```
    ./multi-rename [-t] "target direktori" [-a] [-r] "nama file" "nama baru"
    ./multi-rename [-t] "target direktori" [-d] [-a] [-r] "nama file"
    ```

Skrip ini bekerja pada satu baris perintah.
Lalu skrip akan mencari nama file/direktori dari word/kata yang cocok ("old name") di direktori yang ditentukan.
Jika opsi -a tidak diaktifkan file tersembunyi tidak akan ditargetkan.
mengganti word/kata ("old name") menjadi ("new name") menggunakan substitusi word/kata (pattern  substitution) dari built-in bash.
Jika opsi -r tidak diaktifkan skrip akan mengganti word/kata yang berada diposisi awal.

# INSTALLATION
    curl -s https://codeload.github.com/XklienZ/multi-rename/legacy.tar.gz/master | tar --recursive-unlink --one-top-level=multi-rename --strip-components=1 --extract --gzip && chmod +x multi-rename/multi_rename;
