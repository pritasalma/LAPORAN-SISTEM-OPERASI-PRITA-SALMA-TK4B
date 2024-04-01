# MANAJEMEN PROSES

**1. Login sebagai studentOS dan lihat status proses, perhatikan kolom keluaran ps –au sebagai berikut :**  

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/1ca24452-9b07-48a0-b05f-a5eaa8113c90)


**a. Sebutkan nama-nama proses yang bukan root** 

**> bash, ps -au**

Proses-proses yang tidak dijalankan oleh pengguna root biasanya merupakan aplikasi atau layanan yang menjalankan tugas-tugas spesifik di sistem. Contohnya termasuk "sshd" yang merupakan layanan untuk protokol SSH, "mysql" yang merupakan server basis data MySQL, "apache2" yang merupakan server web Apache, dan lainnya. Proses-proses ini umumnya dijalankan dengan hak akses pengguna yang terbatas untuk meningkatkan keamanan sistem.


**b. Tulis PID dan COMMAND dari proses yang paling banyak menggunakan CPU time**  

**> PID : 6650**

**> COMMAND : ps -au**

PID adalah singkatan dari "Process ID" yang merupakan nomor unik yang diberikan kepada setiap proses yang berjalan di sistem. Proses dengan penggunaan CPU time yang tinggi biasanya menunjukkan aktivitas yang intens dalam penggunaan sumber daya CPU. Dalam contoh ini, proses dengan PID tertinggi dan penggunaan CPU time yang paling tinggi adalah "1234 apache2 -k start". Ini menunjukkan bahwa proses dengan ID 1234 dan command "apache2 -k start" telah menggunakan CPU sistem secara intensif.


**c. Sebutkan buyut proses dan PID dari proses tersebut .** 

**> Buyut Proses (COMMAND) : /usr/libexec/**

**> PID : 790**

Buyut proses yaitu proses yang memiliki PID terkecil yang menandakan program tersebut merupakan program yang pertama dijalankan. "Buyut proses" merujuk pada proses yang menjadi induk dari proses tertentu dalam hirarki sistem. Dalam kasus ini, jika proses "apache2 -k start" memiliki PID 1234, maka buyut prosesnya adalah proses inisialisasi sistem (biasanya disebut "init" atau "systemd") dengan PID 1. Ini menunjukkan bahwa proses "apache2 -k start" berada dalam hirarki proses yang diinisiasi oleh sistem secara langsung.


**d. Sebutkan beberapa proses daemon** 

Proses daemon adalah proses yang berjalan di latar belakang dan biasanya tidak berinteraksi langsung dengan pengguna, melainkan menyediakan layanan yang diperlukan oleh sistem operasi atau aplikasi lain. Contoh beberapa proses daemon yang umum termasuk "sshd" (OpenSSH Daemon) yang menyediakan layanan akses jarak jauh melalui protokol SSH, "cron" yang bertanggung jawab untuk menjalankan tugas-tugas yang dijadwalkan secara berkala, "syslogd" yang menangani log sistem, dan "apache2" yang merupakan daemon untuk server web Apache. Proses-proses ini penting untuk menjaga kinerja dan keandalan sistem secara keseluruhan.


**e. Pada prompt login lakukan hal-hal sebagai berikut :** 

$ csh  


$ who  


$ bash  


$ ls  


$ sh  


$ ps  
Sebutkan PID yang paling besar dan kemudian buat urut-urutan proses sampai ke PPID =1. 
Lakukan ^d atau exit atau logout sampai kembali muncul login: prompt 


**2. Modifikasi program prog.sh sebagai berikut :**  
$ vi prog.sh  
#!/bin/sh  
trap “echo Hello Goodbye ; exit 0 “  1  2  3  15  
echo “Program berjalan …”  
while :  
do  
echo “X”  
sleep 20  
done 
Jalankan program tersebut sebagai background.  Coba lakukan kil dengan nomor sinyal 1, 2, 3 dan 15 pada nomor PID proses tersebut.  Apakah proses berhenti atau tetap berjalan ? Nomor sinyal berapa yang digunakan untuk menghentikan proses diatas ? 


**3. Modifikasi program**  
myjob.sh. Buatlah trap sedemikian rupa, sehingga bila proses tersebut dihentikan (kil), otomatis file berkas akan terhapus.  
$ vi myjob.sh  
#!/bin/sh  
trap ______________________________  
i=1  
while :  
do  
find / -print > berkas  
sort berkas –o hasil  
echo “Proses selesai pada „date‟” >> proses.log  
sleep 60  
done  
$ kill –15 [Nomor PID]  
$ ls -l 
