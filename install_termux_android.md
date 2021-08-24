# Install Ubuntu 20.04 di termux
https://youtu.be/zbdXk1TVfJ4

Termux memungkinkan kita menjalankan perintah-perintah terminal linux, tapi akses dan aplikasi tersedia masih terbatas, karena itu menginstall distro yang sudah umum seperti ubuntu perlu dilakukan.

Chroot adalah jenis aplikasi di unix variannya (termasuk linux dan termux) untuk mensimulasikan akses ke root di mana akses ke root sebenarnya dihindari, contoh di android akses ke root (rooting) bisa mengakibatkan hilangnya garansi device (tablet/smartphone), sehingga kita perlu menggunakan chroot ini untuk bisa menginstall ubuntu. Dalam hal ini kita akan mengistal varian chroot yang tersedia di termux yaitu [proot](https://github.com/termux/proot), bedanya proot dari chroot adalah tidak native sehingga tidak perlu di rooting.

Berikut langkah menginstall ubuntu 20.04
1. Di terminal jalankan `pkg update`, untuk update ke repository supaya dapet aplikasi versi terakhir
2. Di terminal jalankan `pkg install proot`, untuk install proot
3. Di terminal jalankan `pkg install proot-distro` untuk install tool menginstal distro linux.
4. Di terminal jalankan `proot-distro install  ubuntu-20.04` untuk menginstall distro `ubuntu-20.04`, distro lain tersedia adalah  `alpine`, `archlinux`, `debian-buster`, `nethunter`, `ubuntu-18.04` update terakhir bisa dilihat di [wiki proot](https://wiki.termux.com/wiki/PRoot)
5. Di terminal jalankan `proot-distro login ubuntu-20.04` untuk masuk ke ubuntu yang sudah terinstall
