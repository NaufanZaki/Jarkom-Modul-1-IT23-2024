# Jarkom-Modul-1-IT23-2024

| Nama | NRP |
| --------------------- | ----------------------- |
| Naufan Zaki Lugmanulhakim | 5027221065 |
|Monika Damelia Hutapea | 5027221011 |

## 1. ATM or ATP or FTP ?

Pradityo mencoba mengembangkan server ftp, tetapi seseorang mencoba melakukan bruteforce login, bisakah Anda menganalisis apa yang terjadi?

### Flag :

![3  atm atp](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/80c2e465-c592-4fe7-a736-2926be8f42bf)

### Langkah -langkah :

- Input filter "ftp" dan cari login sucesfull (code = 230)

![3  login sukses](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/ff6a3fa6-dfc0-44b2-89da-af369a57bb30)

- Follow dan didapat user dan password yang benar

![3  follow](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/c1773683-bb88-44f6-be4a-c7faeccc5777)

## 2. Evidence

Perusahaan nanomate baru saja kebobolan. Mereka menyewamu untuk mencari tahu bagaimana caranya pelaku bisa masuk.

### Flag :

![2  evidence](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/e11041b8-f249-4f56-be3e-d85248d6d087)

### Langkah -langkah :

- Input  filter "http" dan cari info POST

![2  post](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/bb0ed3d7-848b-475e-871a-85251fa8aa84)

- Follow dan didapat domain di host nanomate-solutions.com

![2  satu](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/1b808f44-d1cb-4b38-9e96-04408ce74a42)

- Didapat info server Apache/2.4.56

![2  dua](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/2016a219-ff49-4118-8117-201da7b1eb26)

- Didapat juga info endpoint

![2  tiga](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/288faff8-25ec-412b-aea9-b348e8fa4322)

- Input filter frame.len == 714

![2  frame](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/5de1f970-79b9-4830-b0d6-9f344095d467)

- Membuka tcp.stream eq 1248 dan follow, didapat info email dan password

![2  empat](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/5359d381-f147-423d-9d16-264b7c7c436f)

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

## 8. Secret 

Temukan pesan rahasia dari attacker

### Flag :

## 9. Fuzz

My website got hacked. Can you analyze this network traffic to help me track the attacker?

### Flag :

![1  fuzz hasil](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/d727764a-49ad-47ca-a4ad-24f8632d7299)

### Langkah -langkah :

- Filter http dan cari info POST didapat IP address 10.33.1.154

![1  http](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/68abae28-40f2-43f7-af16-e756f3c6e550)

- Filter ip.src == 10.33.1.154 dan didapat destination port 80

![image](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/7b37b6a6-af9c-47f1-8394-45dd67bcc33d)

- Di filter http sebelumnya follow dan didapat informasi endpoint

![1  tiga](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/38957b17-9cc2-4b75-b5ee-2372e8dc4a63)

- Didapat juga informasi toolsname

![1  empat](https://github.com/NaufanZaki/Jarkom-Modul-1-IT23-2024/assets/124648489/dbc33f1c-5345-4a6e-a713-3e9234d2aa44)


## 10. Malwaew

Ini adalah network traffic dari salah satu komputer di DPSSI yang terkena malware. Pak Sunhi, memintamu untuk membantu menganalisisnya. Bantulah Pak Sunhi untuk menemukan malware tersebut.

### Flag :

















