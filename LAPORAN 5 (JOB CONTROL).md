# JOB CONTROL


1. Eksekusi seluruh profile yang ada :  
a.  Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :  

**echo “Profile dari /etc/profile”**

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/59682db5-9b23-429a-b2b2-1473595f3986)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/f220ce2a-61a4-4d6c-8952-3652f86de638)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/878fb2a4-4850-483a-bed0-476e42e0dd4c)

b.  Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :  
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :  echo “Profile dari .bash_profile”
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan. 

**/home/stD02001/.bash_profile** 

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/8701ff48-49e5-4f08-aee7-66389decc038)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/f1b635b2-830a-4b78-8081-7aa05ecf7dc4)


**/home/. stD02001/.bash_login**  

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/de492cae-0917-4532-a2b3-b9f04e2134dc)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/1fac40e3-b617-409a-92f5-70e9ae5190e8)


**/home/mahasiswa/.profile** 

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/91c6f630-d6ac-428e-bd92-90060937cdf4)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/2f2b91a6-775a-4131-8c05-0a32a5c9873c)


**/home/mahasiswa/.bashrc**  

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/9c2142e9-57cb-4572-9a16-a9f7d85794f2)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/e7f3ca1e-1e7e-4317-8f05-8a379dc38f72)


c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:     

**Merubah file-file menjadi file executeable**

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/3be045f6-4f67-472d-a969-43c6b96dc4df)


**Menampilkan file-file yang dibuat**

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/65dd4304-0847-493b-91d7-9764deda5081)


**$ su mahasiswa**  
**$ exit**

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/6f60062e-18f7-4434-9a13-fef8ac3480d5)


kemudian gunakan opsi – sebagai berikut :  
**$ su – mahasiswa**   
**$ exit** 

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/29b4856a-f4bb-47f1-bce7-e9b6bd905c6f)

**Jelaskan perbedaan kedua utilitas tersebut :**       
Perbedaan  kedua  utilitas  tersebut  yaitu menampilkan  isi  dari file-file  yang  dibuat  pada    direktori    yang  berbeda.  Untuk  direktori  yang  memiliki  banyak  file,  hanya  akan ditampilkan satu buah filenya saja.


2. Prompt String (PS)
   
a. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:  
Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell  

**PS1=‟> „** 
**export PS1**

b.  Eksperimen hasil PS1 :

$ PS1=“\! > “ 
69 > PS1=”\d > “  
Mon Sep 23 > PS1=”\t > “  
10:10:20 > PS1=”Saya=\u > “  
Saya=mahasiswa > PS1=”\w >”  
~ > PS1=\h >”

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/34490904-21f4-43c6-8558-aacba1baa452)


3. Logout
     
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout  
Echo “Terima kasih atas sesi yang diberikan” 

**Sleep 5**  
**clear**  

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/2b339642-4436-4355-be6a-42eb30d3b2f2)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/c98d223f-c45f-4681-a074-f13af41392d2)

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/fd783243-d791-4b61-b049-2d213b86fdd3)

Untuk mengedit file .bash_logout masuk sebagai user root terlebih dahulu. Lalu masukkan text edit dengan echo beserta waktu tunggu selama 5 detik (5 sleep) dan juga syntax clear yang berfungsi untuk membersikan layar saat file .bash_logout ditampilkan, untuk menampilkan file .bash_logout ubah file menjadi executable terlebih dahulu. Jika file tampil, maka ia akan memeberikan output berupa inputan text yang kita masukkan yaitu Terima kasih atas sesi yang diberikan dan layar akan dibersikan setelah 5 detik.

4. Bash script  
a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :
 
**p1.sh**  
#! /bin/bash  
echo “Program p1”  
ls –l

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/7a1fac51-c8f5-4731-b3ee-fab8ce99286a)


**p2.sh**  
#! /bin/bash  
echo “Program p2”  
who  

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/7be5a496-8d96-4471-b0f1-d37af0dbc04b)


**p3.sh**  
#! /bin/bash  
echo “Program p3”  
ps x  

![image](https://github.com/pritasalma/SISTEM-OPERASI-PRITA-SALMA-TK4B/assets/126141683/8112309a-1c35-4eb5-89a6-7616b6042543)


b.  Jalankan script tersebut sebagai berikut :  

**$  ./p1.sh ; ./p3.sh ; ./p2.sh**


**$  ./p1.sh &**


**$  ./p1.sh $ ./p2.sh & ./p3.sh &**


**$  ( ./p1.sh ; ./p3.sh ) &**
