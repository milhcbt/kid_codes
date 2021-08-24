# Install Ubuntu 20.04 *) di termux
https://youtu.be/zbdXk1TVfJ4  << termux di playstore sudah tidak diupdate, sebaiknya download yang terbaru di https://wiki.termux.com/wiki/Main_Page 

Termux memungkinkan kita menjalankan perintah-perintah terminal linux, tapi akses dan aplikasi tersedia masih terbatas, karena itu menginstall distro yang sudah umum seperti ubuntu perlu dilakukan.

Chroot adalah jenis aplikasi di unix variannya (termasuk linux dan termux) untuk mensimulasikan akses ke root di mana akses ke root sebenarnya dihindari, contoh di android akses ke root (rooting) bisa mengakibatkan hilangnya garansi device (tablet/smartphone), sehingga kita perlu menggunakan chroot ini untuk bisa menginstall ubuntu. Dalam hal ini kita akan mengistal varian chroot yang tersedia di termux yaitu [proot](https://github.com/termux/proot), bedanya proot dari chroot adalah tidak native sehingga tidak perlu di rooting.

Berikut langkah menginstall ubuntu 20.04
1. Di terminal jalankan `pkg update`, untuk update ke repository supaya dapet aplikasi versi terakhir
2. Di terminal jalankan `pkg install proot`, untuk install proot
3. Di terminal jalankan `pkg install proot-distro` untuk install tool menginstal distro linux.
4. Di terminal jalankan `proot-distro install  ubuntu` untuk menginstall distro `ubuntu-20.04`, distro lain tersedia adalah  `alpine`, `archlinux`, `debian-buster`, `nethunter` update terakhir bisa dilihat di [wiki proot](https://wiki.termux.com/wiki/PRoot) *)
5. Di terminal jalankan `proot-distro login ubuntu` untuk masuk ke ubuntu yang sudah terinstall

poin no 5 diatas akan login sebagai `root`, untuk beberapa aplikasi seperti node.js tidak disarankan/diperbolehkan menggunakan `root`. untuk itu bisa membuat user dgn cara sebagai berikut

6. Setelah login sebagai root jalankan perintah `apt update && apt upgrade && apt install sudo -y` untuk install applikasi sudo (mengakses root dari user)
7. Buat usernya sendiri, contoh 'badu', masih sebagai root jalankan perintah `adduser badu`, ikuti dengan menjawab yes, dan password yang dibutuhkan untuk login
8. Supaya bisa berperan sebagai sudoer (bisa install aplikasi), masukan 'badu' jadi 'sodoer' dgn perintah `echo "sammy ALL=(ALL:ALL) ALL" > /etc/sudoers`

setelah itu keluar dulu dengan perintah `exit` kemudian bisa login lagi ke ubuntu dengan perintah `proot-distro login --user badu ubuntu`



*) Alias dari distro bisa terus berubah, di terminal jalankan `proot-distro list` untuk memastikan distro yg tepat untuk proses install sendiri bisa menggunakan format `proot-distro install <alias>`
