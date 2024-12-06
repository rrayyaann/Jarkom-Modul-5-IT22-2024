# Jarkom-Modul-5-IT22-2024

**KELOMPOK IT22**
| Nama | NRP |
|---------------------------|------------|
|Muhamad Arrayyan | 5027231014 |
|Fadlillah Cantika Sari Hermawan ❌ | 5027231042 |

## Prefix IP 
Kelompok kami memiliki prefix IP `192.244`

<details>
<summary>Dokumentasi</summary>

## Dokumentasi Testing
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/4c209241-8f34-427e-a0a6-ec8a06424a2f">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/c8e2602e-7ad1-4ac1-baca-3f79b207408b">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/f3c5cde9-f02e-40e5-a118-07e30b2face9">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/f79031a0-21c4-4230-8ac0-8d1daa47a59a">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/d6d52bbf-8572-461c-ac8c-82b9166574d0">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/9ed2c127-abff-4d47-b189-05aaed744da2">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/8d00b3fc-4d62-4a77-bc28-36750bf826d7">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/cb1bfa64-2553-4406-be5d-0f478825044a">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/3b449f47-5e10-4092-b53c-ac39ccc951ae">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/24b067f9-0385-48ed-a092-8b9ab6b6259c">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/d1f3a853-9676-466d-aba8-13ad84c1387d">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/c3b1c063-a00d-4211-9cc9-d329366250eb">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/21e10e94-eab3-4071-b753-e645a5279f06">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/7aa82a2e-a04e-44ba-98d4-2bba21d96e53">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/628521fb-9106-41ef-bdbb-8c509f2596a3">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/090fb2d8-0740-4c36-bffc-bb60e1ebce00">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/b76469fc-f620-4073-ba8c-1f368ae951ae">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/6f163bfc-bc9d-466d-b97e-ab72c64ea12e">
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/958dfea4-3623-4457-8f16-06bfcad6968b">

</details>

# Spreadsheet
https://docs.google.com/spreadsheets/d/1MhaMOiWueZfxZUgOedcuPsIKiQ-S026za_WP8uIFIH4/edit?usp=sharing

# GNS-VLSM
<details>
<summary>Gambar Topologi GNS-VLSM</summary>
## VLSM Topologi @ GNS3 
<img width="1500" alt="topo-gns" src="https://github.com/user-attachments/assets/3dec0577-b9c7-4ced-a20e-5dc52cfe475e">
</details>

# Subneting
<details>
<summary>Subneting</summary>
## VLSM Topologi @ GNS3 
<img width="1500" alt="topo-gns" src="https://github.com/user-attachments/assets/dccfb792-bbad-43f7-93da-28b869dc8503">
</details>

## RUTE
<details>
<summary>Rute</summary>
<img width="1500" alt="rute" src="https://github.com/user-attachments/assets/4cb0cad2-7f94-4cc6-877d-a7e112fb80b4">
</details>

## PEMBAGIAN IP
<details>
<summary>Pembagian IP</summary>
<img width="1500" alt="pembagian ip" src="https://github.com/user-attachments/assets/12323a71-b037-4c56-b152-bd3033ff4998">
</details>

## TREE
<details>
<summary>Tree</summary>
<img width="1500" alt="tree" src="https://github.com/user-attachments/assets/37485d5f-0b1c-4d59-af89-4a4dd693cce4">
</details>

## Konfigurasi Network
### NewEridu
```jsx
auto eth0
iface eth0 inet dhcp

#A1
auto eth1
iface eth1 inet static
  address 192.244.0.1
  netmask 255.255.255.252
  
#A2
auto eth2
iface eth2 inet static
  address 192.244.0.5
  netmask 255.255.255.252
```

### ScootOutpost
```jsx
#A6
auto eth0
iface eth0 inet static
  address 192.244.2.2
  netmask 255.255.255.248
  gateway 192.244.2.1

#A9
auto eth1
iface eth1 inet static
  address 192.244.2.129
  netmask 255.255.255.252
```

### SixStreet
```jsx
#A1
auto eth0
iface eth0 inet static
  address 192.244.0.2
  netmask 255.255.255.252
  gateway 192.244.0.1

#A6
auto eth1
iface eth1 inet static
  address 192.244.2.1
  netmask 255.255.255.248

#A7
auto eth2
iface eth2 inet static
  address 192.244.2.9
  netmask 255.255.255.248
```

### OuterRing
```jsx
#A6
auto eth0
iface eth0 inet static
  address 192.244.2.3
  netmask 255.255.255.248
  gateway 192.244.2.1

#A8
auto eth1
iface eth1 inet static
  address 192.244.2.65
  netmask 255.255.255.192
```

### HDD (DNS)
```jsx
#A7
auto eth0
iface eth0 inet static
  address 192.244.2.10
  netmask 255.255.255.248
  gateway 192.244.2.9
```

### HollowZero
```jsx
#A9
auto eth0
iface eth0 inet static
  address 192.244.2.130
  netmask 255.255.255.252
  gateway 192.244.2.129
```

### Caesar (Client)
```jsx
auto eth0
iface eth0 inet dhcp
```

### Burnice (Client)
```jsx
auto eth0
iface eth0 inet dhcp
```

### Fairy (DHCP)
```jsx
#A7
auto eth0
iface eth0 inet static
  address 192.244.2.11
  netmask 255.255.255.248
  gateway 192.244.2.9
```

### LuminaSquare
```jsx
#A2
auto eth0
iface eth0 inet static
  address 192.244.0.6
  netmask 255.255.255.252
  gateway 192.244.0.5

#A3
auto eth1
iface eth1 inet static
  address 192.244.0.9
  netmask 255.255.255.248

#A5
auto eth2
iface eth2 inet static
  address 192.244.1.1
  netmask 255.255.255.0
```

### BalletTwins
```jsx
#A3
auto eth0
iface eth0 inet static
  address 192.244.0.11
  netmask 255.255.255.248
  gateway 192.244.0.9

#A4
auto eth1
iface eth1 inet static
  address 192.244.0.129
  netmask 255.255.255.128
```

### HIA
```jsx
#A3
auto eth0
iface eth0 inet static
  address 192.244.0.10
  netmask 255.255.255.248
  gateway 192.244.0.9
```

### Lycaon(Client)
```jsx
auto eth0
iface eth0 inet dhcp
```

### Ellen(Client)
```jsx
auto eth0
iface eth0 inet dhcp
```

### Policeboo (Client)
```jsx
auto eth0
iface eth0 inet dhcp
```

### Jane (Client)
```jsx
auto eth0
iface eth0 inet dhcp
```


## Routing
### NewEridu
```jsx
#KIRI
post-up route add -net 192.244.2.8 netmask 255.255.255.248 gw 192.244.0.2 #A7
post-up route add -net 192.244.2.0 netmask 255.255.255.248 gw 192.244.0.2 #A6
post-up route add -net 192.244.2.128 netmask 255.255.255.252 gw 192.244.0.2 #A9
post-up route add -net 192.244.2.64 netmask 255.255.255.192 gw 192.244.0.2 #A8

#KANAN
post-up route add -net 192.244.0.8 netmask 255.255.255.248 gw 192.244.0.6 #A3
post-up route add -net 192.244.1.0 netmask 255.255.255.0 gw 192.244.0.6 #A5
post-up route add -net 192.244.0.128 netmask 255.255.255.128 gw 192.244.0.6 #A4
```

### ScootOutpost
```jsx
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.2.1 #A1
```

### SixStreet
```jsx
up echo nameserver 192.168.122.1 > /etc/resolv.conf

post-up route add -net 192.244.2.128 netmask 255.255.255.252 gw 192.244.2.2 #A9

post-up route add -net 192.244.2.64 netmask 255.255.255.192 gw 192.244.2.3 #A8
```

### OuterRing
```jsx
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### HDD (DNS)
```jsx
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### HollowZero
```jsx
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.2.129 #A1

up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Fairy (DHCP)
```jsx
up echo nameserver 192.168.122.1 > /etc/resolv.conf

post-up route add -net 192.244.2.64 netmask 255.255.255.192 gw 192.244.2.9 #A8
post-up route add -net 192.244.1.0 netmask 255.255.255.0 gw 192.244.2.9 #A5
post-up route add -net 192.244.0.128 netmask 255.255.255.128 gw 192.244.2.9 #A4
```

### LuminaSquare
```jsx
up echo nameserver 192.168.122.1 > /etc/resolv.conf

post-up route add -net 192.244.0.128 netmask 255.255.255.128 gw 192.244.0.11 #A4
```

### BalletTwins
```jsx
post-up route add -net 192.244.2.8 netmask 255.255.255.248 gw 192.244.0.9 #A7

up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### HIA
```jsx
post-up route add -net 192.244.0.4 netmask 255.255.255.252 gw 192.244.0.9 #A2

up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
## Misi 2 No 1
> New Eridu bisa terhubung ke internet, perlu konfigurasi routing dengan iptables namun tidak diperbolehkan menggunakan MASQUERADE
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/4c209241-8f34-427e-a0a6-ec8a06424a2f">

## Misi 2 No 2
> perangkat lain tidak bisa mengakses fairy, sedangkan fairy bisa mengakses semua perangkat.

lakukan command di Fairy
```jsx
iptables -A INPUT -p icmp --icmp-type echo-request -j DROP
```

## Testing
Fairy ke HIA (bisa ping)
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/c8e2602e-7ad1-4ac1-baca-3f79b207408b">

HIA ke Fairy (Tidak bisa ping)
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/0345238e-966b-45f4-972a-665ff7474ebc">
<img width="1500" alt="dokumentasi" src="">
<img width="1500" alt="dokumentasi" src="">
<img width="1500" alt="dokumentasi" src="">


## Misi 2 No 3
> Hanya Fairy yang dapat mengakses HDD, dan gunakan nc (netcat) untuk memastikan akses

Jalankan semuanya (dhcpnya), kemudian di HDD command
```
iptables -L INPUT -n --line-numbers
```
*untuk melihat mengecek dan memetakan aturan firewall yang mengatur siapa yang boleh masuk ke sistem*

kemudian, blok semua akses perangkat lain dengan command
```
iptables -P INPUT DROP
```

untuk memberikan izin Fairy mengakses HDD (DNS) lakukan command
```
iptables -A INPUT -s 192.244.2.11 -j ACCEPT
```
untuk Drop semua akses lakukan command
```
iptables -D INPUT 1
```

dari Fairy ke HDD (bisa ping)
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/d6d52bbf-8572-461c-ac8c-82b9166574d0">

dari Lumina ke HDD (tidak bisa ping)
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/9ed2c127-abff-4d47-b189-05aaed744da2">

untuk testing dengan netcat, pastikan membuka port yang akan digunakan di HDD
*jangan lupa untuk restart HDD dan install netcat dulu `apt-get update` dan `apt-get install netcat`* kemudian lakukan blok kayak diatas dan testing netcat dengan command di HDD:
```
nc -l -p 3030
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/24b067f9-0385-48ed-a092-8b9ab6b6259c">

testing pada fairy dengan command
```
echo "pesan" |nc 192.244.2.10 3030
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/d1f3a853-9676-466d-aba8-13ad84c1387d">

lalu balik lagi ke  HDD <br>
**Berhasil*
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/c3b1c063-a00d-4211-9cc9-d329366250eb">

## Misi 2 No 4
> Hollow hanya boleh diakses pada hari Senin hingga Jumat dan hanya oleh faksi SoC (Burnice & Caesar) dan PubSec(Jane & Policeboo). karena hari ini hari sabtu, mereka harus menunggu hingga hari senin. Gunakan curl untuk memastikan akses ini.

Masuk ke Web console HollowZero dan run setup.sh
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/21e10e94-eab3-4071-b753-e645a5279f06">

cek untuk mencoba webservernya
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/7aa82a2e-a04e-44ba-98d4-2bba21d96e53">

command untuk drop semua akses
```
iptables -P INPUT DROP
```

command untuk mengizinkan A8 dan A5 mengakses Hollow
```
iptables -A INPUT -s 192.244.2.64/26 -m time --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
iptables -A INPUT -s 192.244.1.0/24 -m time --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```

Testing jika **SoC (Burnice & Caisar)** di Accept pada Mon,Tue,Wed,Thu,Fri sedangkan `date` sekarang adalah wed dengan command
```
iptables -A INPUT -s 192.244.2.64/26 -m time --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/628521fb-9106-41ef-bdbb-8c509f2596a3">

**Date hari ini (wed)*
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/090fb2d8-0740-4c36-bffc-bb60e1ebce00">

maka, SoC (Burnice & Caesar) dapat mengakses
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/b76469fc-f620-4073-ba8c-1f368ae951ae">

Sedangkan, PubSec (Jane & Policeboo) tidak dapat mengakses
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/6f163bfc-bc9d-466d-b97e-ab72c64ea12e">

## Misi 2 No 5
> HIA hanya dierbolehkan untuk 
a. Ellen dan Lycaon pada jam 08.00-21.00
b. Jane dan Policeboo pada jam 03.00-23.00.
Gunakan Curl untuk memastikan akses ini

Masuk ke Web console HIA dan run setup.sh
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/ca85852c-4cd6-40f8-8090-9522bf5b33bf">

cek untuk mencoba webservernya
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/eb44337e-c013-4790-9924-f31e31d347d9">

jalankan iptables 
```
iptables -P INPUT DROP
```
```
iptables -A INPUT -s 192.244.0.128/25 -m time --timestart 08:00 --timestop 21:00 -j ACCEPT 
iptables -A INPUT -s 192.244.1.0/24 -m time --timestart 03:00 --timestop 23:00 -j ACCEPT
```
Waktu sekarang (saat saya testing)
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/2c476ca3-ea67-4cb4-9782-6441cff604f1">

Testing Jika **Lycaon dan Ellen** di Accept pada 08:00 --timestop 21:00 (jam saat ini, 19.00-an) dengan command
```
iptables -P INPUT DROP
```
```
iptables -A INPUT -s 192.244.0.128/25 -m time --timestart 08:00 --timestop 21:00 -j ACCEPT 
```

maka, Lycaon dan Ellen bisa mengakses, dikarenakan masih dalam range jamnya
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/4f97ace8-7edb-4356-8250-9fd6d5017f18">

sedangkan, Jane dan Policeboo tidak dapat mengakses karena akses masih untuk Lycaon dan Ellen
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/6c9f43f5-bc28-4fcf-b9d5-f27718c98a08">

Testing Jika **Jane & Policeboo** di Accept pada 08:00 --timestop 21:00 (jam saat ini, 19.00-an) dengan command
```
iptables -A INPUT -s 192.244.1.0/24 -m time --timestart 03:00 --timestop 23:00 -j ACCEPT
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/7fa2c962-f1fa-4cfb-baf5-bfd355d6c8e4">

jangan lupa untuk drop iptables Lycaon dan Ellen terlebih dahulu untuk memastikan testing akses hanya untuk Jane & Policeboo
```
iptables -D INPUT 1
```

maka, Jane & Policeboo bisa mengakses, dikarenakan masih dalam range jamnya
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/c6462c45-9c39-4043-acc4-5931c15cc6e8">

sedangkan, Lycaon dan Ellen tidak dapat mengakses karena akses masih untuk Jane & Policeboo
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/a0435e29-34a2-4ba9-8dbe-c583ec74353e">

## Misi 2 No 6
> PubSec (Jane & Policeboo) diminta meperketat keamanan jaringan server HIA. Pubsec melakukan simulasi port scan menggunakan nmap pada rentang port 1-100
a. Web server harus memblokir aktivitas scan port yang melebihi 25 port secara otomatis dalam rentang waktu 10 detik
b. penyerang yang terblokir tidak dapat melakukan ping, nc, atau curl ke HIA
c. Catat Log dari Iptables untuk keperluan analisis dan dokumentasikan dalam format PDF

aktifkan HIA dengan `bash setup.sh`
kemudian run IPTABLES
**cat pada setup.sh di HIA* atau salin dibawah ini
```
#Create a chain for handling port scanning
iptables -N PORTSCAN

#Detect and handle new connections to ports 1-100
iptables -I INPUT 1 -j LOG --log-prefix "PORT SCAN BRO: " --log-level 4 --log-tcp-options --log-ip-options

iptables -A INPUT -p tcp --dport 1:100 -m state --state NEW -m recent --set --name portscan

iptables -A INPUT -p tcp --dport 1:100 -m state --state NEW -m recent --update --seconds 10 --hitcount 25 --name portscan -j PORTSCAN

#Log and block port-scanning IPs
iptables -A PORTSCAN -m recent --set --name blacklist
iptables -I PORTSCAN 1 -j LOG --log-prefix "PORT SCAN DETECTED: " --log-level 4 --log-tcp-options --log-ip-options
#iptables -A PORTSCAN -j DROP

#Block all further traffic from blacklisted IPs
#iptables -A INPUT -m recent --name blacklist --rcheck -j DROP
#iptables -A OUTPUT -m recent --name blacklist --rcheck -j DROP
```

policeboo ping & curl
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/35d76587-d84a-4b36-bdd1-e12d448aebe2">

kemudian, kita policeboo Nmap ke HIA
```
nmap -p 1-100 192.244.0.10
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/7dcdc81d-5cbb-4322-bf55-a0288977c64b">

setelah itu kita coba ping dan curl policeboo
**tidak bisa*
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/acbb7b3e-0117-4319-b9a0-ded1db104028">

sedangkan, Jane tetap bisa ping dan curl karena dia tidak menyerang

## Misi 2 No 7
> Akses Hollow hanya boleh berasal dari 2 koneksi aktif dari 2 IP yang berbeda dalam waktu bersamaan. Burnice, Caesar, Jane, dan Policeboo diminta melakukan uji coba menggunakan curl.

jalankan `bash setup.sh` <br>
kemudian, iptables di Hollow Zero
```
iptables -A INPUT -p tcp --dport http -m conntrack --ctstate NEW -m recent --set

iptables -A INPUT -p tcp --dport http -m conntrack --ctstate NEW -m recent --update --seconds 1 --hitcount 3 -j REJECT

iptables -A INPUT -p tcp --dport http -j ACCEPT
```

### Testing
sebelumnya pastikan sudah menginstal paralel di tempat kita mau command
```
apt-get update
apt-get install parallel -y
```

kemudian, testing di client antara Caesar, Burnice, Jane atau Policeboo. disini saya saya testing di Jane
```
parallel curl -s http://IP-HollowZero ::: IP-Caesar IP-Burnice IP-Jane IP-Policeboo
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/9b17e58c-1073-4ca5-a80a-ae8e85ac571d">

### Misi 2 No 8
> setiap paket yang dikirim Fairy ke Burnnice ternyata dialihkan ke HollowZero. Gunakan nc untuk memastikan alur pengalihan ini

jalankan command di Burnice
```
iptables -t nat -A PREROUTING -p tcp --dport 3030 -j DNAT --to-destination 192.244.2.130

iptables -t nat -A POSTROUTING -p tcp --dport 3030 -j MASQUERADE
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/d1d1759d-56e9-4cbd-8ed6-eeab641af516">

### Testing
command di Hollow Zero
*jangan lupa install netcat dulu `apt-get update` dan `apt-get install netcat`*
```
nc -l -p 3030
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/7ddf275e-112d-4565-bd80-fceeb151c80b">

dari fairy netcat ke burnice
```
echo "burnice apa holow" | nc [IP burnice] 3030
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/f38a4f2d-0654-43a0-addd-bb555e8d3fa2">

kemudian ke Hollow lagi untuk liat hasilnya
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/1cb5bb2a-5ee6-4d4c-add7-287b3c8d29c4">

### Misi 3
> memblokir semua transmisi masuk maupun keluar dari Burnice bisa memanipulasi policy iptables. Sebelum Burnice sepenuhnya terisolasi, Fairy mengirimkan pesan moral: “Kepercayaan adalah dasar dari jaringan yang aman. Jangan pernah mengkhianatinya.

di burnice

```
apt-get update

apt install netcat -y

nc -l -p 3030
```

di fairy kirim pesan
```
echo "Kepercayaan adalah dasar dari jaringan yang aman. Jangan pernah mengkhianatinya" | nc [ip burnice] 3030
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/4621f216-c06a-4bcb-9833-dcefad680cb1">

kembali ke burnice untuk melihat hasilnya
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/271e3d25-0613-42e9-92de-1f7b0b5bd54a">

kemudian, jalankan command berikut di burnice
```
iptables -P INPUT DROP
iptables -P OUTPUT DROP
iptables -P FORWARD DROP
```
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/c90a12ec-c5cb-49d6-aa41-6e258ca41bd6">

perangkat lain tdak bisa ping burnice
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/526ca2b5-0452-4798-9ec0-8cb3fd3d31df">

burnice tidak bisa ping keluar
<img width="1500" alt="dokumentasi" src="https://github.com/user-attachments/assets/8aa9aa39-4581-432e-a914-297ae1ccdffa">

## SELESAI - TERIMAKASIH
