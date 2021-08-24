# Install Jupyter Notebook

Video sebelumnya kalau belum ada ubuntu/termux di androidnya. https://youtu.be/l10780LEOP4

Jupyter Notebook adalah media(aplikasi) yang memungkinkan kita menggunakan bahasa programming
secara interaktif, hingga membuat belajar pemograman lebih mudah.

Berikut langkah menginstall(memasang) jupyter lengkap dgn numpy dan mathplotlib
1. Masuk ke ubuntu di termux dgn perintah `proot-distro login ubuntu-20.04` *)
2. Memastikan dapet versi terbaru, update repo dgn perintah `apt update`
3. Install (memasang) python 3 dan dev(elopment) toolnya di ubuntu, `python3-pip python3-dev`
4. Update pip (software untuk mengatur module python) dgn perintah `pip3 install --upgrade pip`
5. Install virtual enviroment supaya satu program pythonn tdk bentrok dgn python lainnya tidak bentrok2 `pip3 install virtualenv`
6. Membuat folder untuk jupyter, `mkdir jupyter`
7. Masuk ke folder jupyter yang baru dibuat `cd jupyter`
8. Menyiapkan virtual enviroment python buat jupyter `virtualenv enviroment`
9. Mengaktifkan virtual enviroment `source enviroment/bin/activate`
10. Install Jupyter `pip install jupyter`
11. Installasi Jupyter sudah selesai, untuk menjalankan jupyter notebook jalankan perintah `jupyter notebook --allow-root`. normalnya tidak harus pakai `--allow-root` tapi karena ubuntu pakai proot ini selalu root (administrator), jadi harus pakai opsih `--allow-root`
12.  Selanjutnya untuk perhitungan matematika dan bikin graph/diagram butuh library numpy dan matplotlib. install numpy `pip install numpy`, install mathplotlib `pip install mathplotlib`, `pip install wheel' hanya dijalankan kalau belum ada, tapi dalam video sudah ada dari modul sebelumnya jadi tidak dibutuhkan.
13. Installl numpy dan matplotlib dengan perintah `pip install numpy matplotlib`


info detail tentang sbb
- jupyter  di https://jupyter.org/
- numpy di https://numpy.org/
- mathplot di https://matplotlib.org/
  

*)sesuaikan dgn nama distro, waktu video dibuat namanya` ubuntu-20.04`, saat ini `ubuntu`
