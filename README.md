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






