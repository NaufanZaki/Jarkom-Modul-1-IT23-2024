# Jarkom-Modul-1-IT23-2024

| Nama | NRP |
| --------------------- | ----------------------- |
| Monika Damelia Hutapea | 5027221011 |
| Naufan Zaki Lugmanulhakim | 5027221065 |

## 1. ATM or ATP or FTP ?

Pradityo mencoba mengembangkan server ftp, tetapi seseorang mencoba melakukan bruteforce login, bisakah Anda menganalisis apa yang terjadi?

### Flag :

![3  atm atp](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/80c2e465-c592-4fe7-a736-2926be8f42bf)

### Langkah -langkah :

- Input filter "ftp" dan cari login sucesfull (code = 230)

![3  login sukses](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/ff6a3fa6-dfc0-44b2-89da-af369a57bb30)

- Follow dan didapat user dan password yang benar

![3  follow](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/c1773683-bb88-44f6-be4a-c7faeccc5777)


## 3. How Many Packets?

Sebagai kewajiban untuk laporan, aku diminta untuk mencari tahu berapa kali attempt login yang dilakukan oleh hacker. Dapatkah kamu membantuku untuk menganalisanya?

### Flag :

![4  how many packages](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/2de84c06-a4ae-48fe-bb60-908caaeb338b)

### Langkah -langkah :

- Input filter FTP dan cari length dari login incorrect

![4  login incorrect](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/0887fbf1-0bd9-452d-82f7-0a997991d532)

- Buka statisic (di bagian atas), kemudian ke packet length, pada display filter input frame.len == 94 dan didapat total attempt sebanyak 934

![4  94](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/96108093-a2a5-4e11-842b-33c9673c262c)

## 4. Trace Him

Selain menghitung jumlah packet, coba lacak juga ip penyerang tersebut!

### Flag :

![5  trace him](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/511778ca-aab9-49c2-81a0-15e9abc348ea)

### Langkah -langkah :

- Input filter ftp dan cari info request, didapat IP ny 10.30.3.4

![5  ip](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/6d9d1810-5f45-4205-8889-8e4e8478f402)

## 5. Creds

Attacker menyadari jika dia bisa membuat clone ftp server dari target, temukan kredensialn dari server ftp yang dibuat oleh attacker

### Flag :

![6  creds](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/e1b1b83e-16c0-4cf3-af78-74ad63bf3284)

### Langkah -langkah :

- Input filter "ftp" dan cari info Login successful (code = 230)

![6  login sukses](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/98044c7f-c9a8-4644-b679-03f2f3d8b7fa)

- Follow dan didapat informasi user dan password

![6  user pw](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/8272b135-282f-4fcd-9006-f496133c3896)

## 6. Malwleoleo

Dapatkah kamu menemukan file malware yang dikirim oleh attacker melalui ftp?

### Flag :

![7  malwleowleo](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/f74b16df-4891-4498-aa72-8577ee94f49c)

### Langkah -langkah :

- File malware terdapat di hasil follow tcp.stream eq 2 sebelumnya

![7  malware](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/2ac4b6ae-2fe8-4844-bcab-919f5dfd9e7c)

## 7. WhoAmI

Dapatkah kamu menemukan siapa identitas attacker?

### Flag : 
![8  Paul](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/48ef9416-4d05-461b-b8a8-8cc6cad042c3)

### Langkah -langkah :

- Melakukan pencarian tcp. stream dan menemukan {} di tcp.stream eq 7

![8  lagi](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/ca764ed3-2a6f-4630-aa06-5fd1c26e7866)

- Melakukan decode di base 64 dan didapat namanya Paul Atreides

![8  whoami](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/2f93b57a-9531-4a6b-9397-d3ec70f72f6c)

## 8. Secret 

Temukan pesan rahasia dari attacker

### Flag :

![9  secret](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/d23ad4a1-0d36-4b6c-8ac4-e77e0b96e64e)

### Langkah -langkah :

- Menginputkan filter ftp-data untuk melihat data apa saja yang ada, didapatkan ada 2 file yaitu m4L1c10us_W4re.c dan mirza.jpg

![image](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/b2ed085e-6274-4505-bcdb-f59998b0952b)

- Unduh file untuk melihat isi data dengan cara klik file (atas kiri), pilih export object, lalu FTP-DATA, dan save file yag dipilih

![image](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/e9e98901-fa67-44cf-8c86-060bf86cf9f4)

- Didapatkan pesan rahasia attacker yaitu MIO MIRZA

![image](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/3b016be4-c1c4-4e10-b6ae-43837a2da47a)
















