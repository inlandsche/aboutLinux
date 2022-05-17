# Starter Pack

Berisi rangkuman materi mengenai *Command Line* pada Linux dan Bash *Scripting* 




&nbsp;
## Linux Tutorial
Tutorial ini berisi beberapa hal penting yang harus dipahami oleh pengguna Linux

## Contents
  - [[1] Command Line](#1-command-line)
    - [[a] Navigasi](#a-navigasi)
    - [[b] File](#b-file)
    - [[c] Manual Page](#c-manual-page)
    - [[d] File Manipulation](#d-file-manipulation)
    - [[e] Vi Text Editor](#e-vi-text-editor)
    - [[f] Wildcards](#f-wildcards)
    - [[g] Permissions](#g-permissions)
    - [[h] Filters](#h-filters)
    - [[i] Grep](#i-grep)
    - [[j] Piping and Redirection](#j-piping-and-redirection)
    - [[k] Process Management](#k-process-management)
  - [[2] Bash Scripting](#2-bash-scripting)
    - [[a] Introduction](#a-introduction)
    - [[b] Create a Bash Script](#b-create-a-bash-script)
    - [[c] Variables](#c-variables)
    - [[c] User Input](#c-user-input)
    - [[d] Arithmetic](#d-arithmetic)
    - [[e] If Statements](#e-if-statements)
    - [[f] Loops](#f-loops)
    - [[g] Function](#g-function)

&nbsp;
### [1] Command Line
Command line merupakan baris perintah yang dapat kita jalankan dengan menggunakan sebuah media. Pada Linux, untuk menjalankan perintah atau *command*, digunakan sebuah *system software* yang bernama **Terminal**. Untuk membuka **Terminal**, kita hanya perlu menuju ke Menu *Applications - Utilities - Terminal*.

Di dalam **Terminal** terdapat **shell** yang merupakan bagian dari OS yang menentukan apa yang akan dilakukan terminal setelah mendapatkan perintah dari *user*. Terdapat berbagai shell yang tersedia, tetapi **shell** yang paling populer adalah **bash** atau **bourne again shell**.

Command atau perintah pada linux terbagi menjadi beberapa kategori sebagai berikut.

#### [a] Navigasi
Terdapat beberapa perintah pada kategori ini.

  * `pwd` , memiliki fungsi untuk melihat direktori yang kita tempati
  * `ls` , memiliki fungsi untuk melihat keseluruhan isi pada suatu direktori. Perintah ini memiliki beberapa atribut tambahan misalnya `ls -a` yang digunakan untuk melihat keseluruhan isi (termasuk hidden files)
  * `cd` , dapat digunakan untuk berpindah ke direktori lain, salah satu cara penggunaannya adalah  ```cd [nama direktori]```

Dalam penggunaan command tersebut, terdapat suatu istilah yang disebut dengan **path** atau jalur. Terdapat beberapa atribut tambahan yang dapat digunakan untuk melengkapi command tersebut.

  * `~` (tilde), merupakan *shortcut* untuk direktori awal atau home. Contoh penggunaanya, ```ls ~/Picture```
  * `.` (dot), menunjukkan direktori saat ini. 
  * `..` (dotdot), merepresentasikan direktori sebelumnya, contoh penggunaannya ```cd ..```

#### [b] File
Perintah `file` merupakan perintah yang berkaitan dengan suatu file atau berkas. Perintah ini memiliki fungsi salah satunya untuk mengidentifikasi jenis suatu file. Penggunaan perintah untuk membuka suatu direktori atau file perlu memperhatikan *case sensitive*. Misalkan terdapat suatu file atau direktori bernama Tugas Besar. Untuk membukanya dapat menggunakan tanda kutip atau menggunakan backslash ( \ ), contohnya ```cd Tugas\ Besar``` 

#### [c] Manual Page
Manual page berisi petunjuk penggunaan serta informasi yang berkaitan terhadap suatu perintah. 

Untuk melihat manual page suatu perintah dapat menggunakan perintah&nbsp; ```man [perintah]```. Perintah `man` juga memiliki atribut tambahan seperti&nbsp; ``man -k <search> ``&nbsp; yang berfungsi untuk mencari suatu kata yang hendak dicari.

#### [d] File Manipulation
Terdapat beberapa command yang berkaitan dengan manipulasi suatu file.

  * `mkdir` , berfungsi untuk membuat direktori baru. Format penggunaannya adalah ```mkdir FolderBaru```
  * `rmdir` , berfungsi untuk menghapus suatu direktori, misalnya ```rmdir FolderBaru```
  * `touch` , berfungsi untuk membuat suatu file kosong, misalnya ```touch newFile```
  * `cp` , berfungsi untuk menyalin suatu direktori atau file, misalnya ```cp newFile ~/Documents``` untuk menyalin file newFile ke direktori Documents
  * `mv` , berfungsi untuk memindahkan suatu file atau direktori, penggunaannya mirip dengan command `cp`
  * `rm` , berfungsi untuk menghapus suatu file, perintah ini tidak dapat digunakan untuk menghapus suatu direktori

#### [e] Vi Text Editor
Vi Text Editor atau sering disebut dengan Vim merupakan salah satu text editor yang terdapat pada *system program* dan dapat diakses dengan menggunakan command `vi`. Untuk mengedit sebuah file dengan Vim, digunakan perintah ```vi <file>```.

Setelah membuat suatu file text, kita perlu menggunakan suatu perintah yang dapat melihat isi file tersebut. Terdapat perintah &nbsp;`cat` dan `less`. Perintah `cat` digunakan untuk membuka keseluruhan isi file sekaligus, sedangkan perintah `less` akan membuka file secara sedikit demi sedikit.

#### [f] Wildcards
Wildcards atau karakter pengganti merupakan sekumpulan blocks yang dapat digunakan untuk merepresentasikan sekumpulan file atau direktori. 

Terdapat beberapa set dasar dari wildcards.

* `\*` merepresentasikan nol karakter atau lebih
* `?` merepresentasikan satu karakter
* `[]` merepresentasikan sebuah jangkauan dari karakter

#### [g] Permissions
Permissions atau perizinan terbagi menjadi tiga bagian, yaitu

  * `r` (read), artinya user dapat melihat atau membuka suatu file atau direktori
  * `w` (write), artinya user dapat mengganti atau memodifikasi isi dari suatu file atau direktori
  * `x` (execute), artinya user dapat mengeksekusi jika file tersebut merupakan sebuah program atau script.

Dalam perizinan, user dapat terbagi menjadi tiga bagian yaitu

  * **owner**, merupakan user yang memiliki suatu file atau yang membuat file tersebut
  * **group**, merupakan sekumpulan uuser yang dapat mengakses suatu file atau direktori
  * **other**, merupakan seluruh user yang tidak termasuk kedalam group dan owner

Terdapat beberapa perintah berkaitan dengan perizinan atau permissions.

  * ```ls - l``` , digunakan untuk melihat isi suatu direktori disertai dengan informasi perizinan.
  * `chmod` , digunakan untuk menrubah suatu perizinan pada file atau direktori.

#### [h] Filters
Terdapat beberapa command yang dapat digunakan untuk membuka isi suatu file dengan beberapa variasi.

  * `head` , perintah ini digunakan untuk meilhat isi bagian atas dari suatu file. Misalnya, &nbsp;```head -2 file.txt```, artinya akan melihat isi dari file.txt dari baris awal hingga baris ke dua.
  * `tail` , perintah ini merupakan kebalikan dari perintah head. Perintah `tail` digunakan untuk melihat isi bagian bawah dari suatu file dari.
  * `sort` , berfungsi untuk mengurutkan isi file sesuai abjad
  * `nl` , berfungsi untuk menampilkan nomor pada tiap baris
  * `wc` , berfungsi untuk menghitung jumlah kata yang terdapat pada suatu file
  * `cut` , berfungsi untuk memotong isi dalam suatu file
  * `sed` , berfungsi untuk melakukan pencarian dan penggantian data pada file.
  * `uniq` , berfungsi untuk menghapus data yang sama pada suatu file
  * `tac` , berfungsi untuk membuka suatu file dari bagian bawah.

#### [i] Grep
Grep merupakan perintah yang digunakan untuk mencari suatu kata pada file atau direktori. Misalnya, ```egrep 'kucing' hewan.txt```, artinya mencari kata kucing pada file hewan.txt.

#### [j] Piping and Redirection
Setiap program yang berjalan memiliki tiga aliran data yaitu STDIN (0) atau Standar Input, STDOUT (1) atau Standar Output, dan STDERR (2) atau Standar Error.


Terdapat beberapa atribut tambahan yang memiliki fungsi tersendiri.

**Redirection**


  * `>` , digunakan untuk menyimpan output menjadi sebuah file, misalnya ```cat file1 > file2``` yang berfungsi untuk menyimpan output file1 ke dalam file baru bernama file2
  * `>>` , digunakan untuk menambahkan output ke dalam sebuah file
  * `<` , digunakan untuk membaca input dari suatu file
  * `2>` , digunakan untuk melihat pesan error yang terjadi


**Piping**

  * `"|"` , digunakan untuk melakukan suatu perintah tambahan terhadap perintah utama, misalnya ```ls | tail -1``` yang berarti melihat keseluruhan isi dari suatu direktori dan melihat data atau isi paling akhir. Output pada perintah ini adalah data paling akhir. Dapat disimpulkan bahwa perintah tambahan setelah tanda | akan menjadi output.

#### [k] Process Management
Terdapat beberapa perintah yang berkaitan dengan manajemen suatu proses.

  * `top` , berfungsi untuk melihat proses yang sedang berjalan secara *real-time*. Dengan perintah tersebut, kita dapat melihat penggunaan *resources* oleh suatu proses
  * `ps` , berfungsi untuk melihat list dari proses yang sedang berjalan
  * `kill` , berfungsi untuk menghentikan suatu proses yang sedang berjalan
  * `jobs` , berfungsi untuk memperlihatkan jobs yang sedang berjalan pada background
  * `fg` , berfungsi untuk memindahkan proses pada background ke foreground


### [2] Bash Scripting
Bash scripting akan mempermudah kita dalam menyelesaikan berbagai permasalahan dan pekerjaan.


#### [a] Introduction
Bash atau bourne again shell merupakan bahasa command line. Untuk mempermudah dalam berbagai hal, kita dapat membuat suatu script dengan menggunakan bash atau biasa disebut dengan **Bash Script**. Bash Script pada linux berisi berbagai perintah linux dengan struktur logic. 

#### [b] Create a Bash Script
Untuk membuat suatu bash script pada linux, kita dapat menggunakan suatu text editor seperti nano text editor atau yang lainnya. Script bash disimpan dengan ekstensi `file.sh` . Untuk menjalankan script yang telah dibuat, kita dapat menggunakan perintah `./file.sh` . Dalam pembuatan bash script, terdapat hal yang harus ada yaitu **Shebang (#!)**.

Shebang berada pada baris pertama bash script, dapat ditulis dengan ``#!/bin/bash`` . Shebang merepresentasikan **path** atau jalur bash yang bertujuan agar script dapat dieksekusi.

#### [c] Variables
Variabel pada bash dapat ditulis dengan format sebagai berikut.

>```variable=value```

>`var='Hello World'`

Isi atau value dari sebuah variabel dapat berupa perintah pada linux misalnya

>`var=$( command )`

Pada bash script terdapat beberapa variabel khusus

- `$0` - Nama bash script.
- `$1` - $9 - 9 argumen pertama pada script. 
- `$#` - banyak argumen yang diteruskan pada script.
- `$@` - Seluruh argumen yang diberikan pada script.
- `$?` - Exit status dari proses yang paling baru dijalankan.
- `$$` - ID proses dari script.
- `$USER` - username dari pengguna yang menjalankan script.
- `$HOSTNAME` - Nama host tempat script dijalankan.
- `$SECONDS` - Jumlah waktu (detik) sejak script dijalankan.
- `$RANDOM` - Mengembalikan nomor acak berbeda.
- `$LINENO` - Mengembalikan nomor baris saat ini pada script Bash.

#### [c] User Input
Untuk mengambil input dari user, digunakan beberapa perintah 

  * `read` , digunakan untuk mengambil input dari user secara langsung
  * `/dev/stdin` , digunakan untuk mengambil input dari suatu file

Contoh penggunaannya

```bash
    #!/bin/bash
    read userName
    echo Hello, $userName
```

Program tersebut akan meminta input dari user dan akan mengeluarkan output Hello, [input] misalnya kita menginput "Guys", maka program akan menghasilkan output "Hello, Guys".

#### [d] Arithmetic
Untuk membuat program dengan mengggunakan perhitungan matematika, dapat menggunakan beberapa perintah ini.

- `let` , berfungsi untuk membuat suatu variabel aritmatik. Contoh penggunaannya, ```let x=5+5```
- `expr` , berbeda dengan let, expr akan secara langsung menjadi variabel, contoh penggunaannya, ```expr 5 + 5```
- `$(( expression ))` , memiliki fungsi yang sama, tetapi membutuhkan variabel untuk menginisialisasi, contoh penggunaannya, ```x=$(( 5+5 ))```
- `$(#variabel)` , berfungsi untuk mencari panjang atau *length* dari suatu variabel

#### [e] If Statements
Penggunaan if statements secara sederhana pada bash adalah sebagai berikut.

```bash
    if [ <some test> ]
    then
    <commands>
    else
    <commands>
    fi
```

Pada if statement, terdapat beberapa operator yang dibedakan berdasarkan tipe data.

**Operator Integer**

- `bil1 -eq bil2` TRUE jika bil1 sama dengan bil2
- `bil1 -ne bil2` TRUE jika bil1 tidak sama dengan bil2
- `bil1 -lt bil2` TRUE jika bil1 lebih kecil dari bil2
- `bil1 -le bil2` TRUE jika bil1 lebih kecil atau sama dengan bil2
- `bil1 -gt bil2` TRUE jika bil1 lebih besar dari bil2
- `bil1 -ge bil2` TRUE jika bil1 lebih besar atau sama dengan bil2

**Operator untuk String**

- `-z var` , bernilai TRUE jika panjang var bernilai zero atau tidak ada teks.
- `var1 == var2` , bernilai TRUE jika var1 sama dengan var2


**Operator untuk File**

- `-f FILE` bernilai TRUE jika FILE ada
- `-d FILE` bernilai TRUE jika FILE ada dan merupakan sebuah directory
- `-r FILE` bernilai TRUE jika FILE ada dan permission read aktif
- `-w FILE` bernilai TRUE jika FILE ada dan permission write aktif
- `-x FILE` bernilai TRUE jika FILE ada dan permission execute aktif

**Operator Boolean**

- **and** - `"&&"` , bernilai TRUE jika semuanya memenuhi
- **or** - `"||"` , bernilai TRUE jika salah satu satu memenuhi

Selain if else, terdapat perintah `case` yang mempunyai fungsi mirip dengan if else. Penggunaannya adalah sebagai berikut.

```bash
    case <variable> in
      <pattern 1>)
      <commands>
    ;;
      <pattern 2>)
      <other commands>
    ;;
    esac
```

#### [f] Loops
Loop atau perulangan pada bash terdiri dari beberapa jenis yaitu

**while loops**
Cara penggunaan while loop adalah sebagai berikut. Perulangan akan berhenti apabila nilai dari statement FALSE.

```bash
    while [ <some test> ]
    do
    <commands>
    done
```

**until loops**
Cara penggunaan until loop mirip dengan while loop. Perulangan akan berhenti apabila nilai dari statement FALSE.

```bash
    until [ <some test> ]
    do
    <commands>
    done
```

**for loops**
Cara kerja for loop hampir sama dengan jenis perulangan sebelumnya. For loop akan melakukan perulangan dari sebuah range. Perulangan akan selesai apabila seluruh data telah dimuat.

```bash
    for var in <list>
    do
    <commands>
    done
```

Pada seluruh jenis perulangan tersebut, terdapat perintah tambahan yaitu

- `break` , berfungsi untuk keluar dari perulangan yang sedang berjalan
- `continue` , akan kembali melakukan perulangan tetapi tidak mengerjakan perintah di bawahnya
- `select` , digunakan untuk membuat suatu menu sederhana

#### [g] Function
Pada bash, function atau fungsi digunakan untuk membuat suatu fungsi tambahan yang dapat memudahkan dalam menyelesaikan permasalahan. Penggunaannya adalah sebagai berikut.

```bash
    function_name () {
      <commands>
    }
```

```bash
    greetings(){
      echo Good Morning
    }
```

ketika fungsi `greetings()` dipanggil, maka akan menghasilkan output "Good Morning". 
Dalam suatu fungsi, dapat ditambahkan return value pada akhir fungsi. Function pada bash juga dapat dilakukan Override.
