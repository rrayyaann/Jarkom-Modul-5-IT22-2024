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

## VLSM Topologi @ GNS3 
<img width="1500" alt="topo-gns" src="https://github.com/user-attachments/assets/dccfb792-bbad-43f7-93da-28b869dc8503">

![image](https://github.com/user-attachments/assets/c8e2602e-7ad1-4ac1-baca-3f79b207408b)
![image](https://github.com/user-attachments/assets/f3c5cde9-f02e-40e5-a118-07e30b2face9)
![image](https://github.com/user-attachments/assets/f79031a0-21c4-4230-8ac0-8d1daa47a59a)
![image](https://github.com/user-attachments/assets/d6d52bbf-8572-461c-ac8c-82b9166574d0)
![image](https://github.com/user-attachments/assets/9ed2c127-abff-4d47-b189-05aaed744da2)
![image](https://github.com/user-attachments/assets/8d00b3fc-4d62-4a77-bc28-36750bf826d7)
![image](https://github.com/user-attachments/assets/cb1bfa64-2553-4406-be5d-0f478825044a)
![image](https://github.com/user-attachments/assets/3b449f47-5e10-4092-b53c-ac39ccc951ae)



</details>

# Spreadsheet
https://docs.google.com/spreadsheets/d/1MhaMOiWueZfxZUgOedcuPsIKiQ-S026za_WP8uIFIH4/edit?usp=sharing

# GNS-VLSM
<details>

<summary>Gambar Topologi GNS-VLSM</summary>

## VLSM Topologi @ GNS3 
<img width="1500" alt="topo-gns" src="https://github.com/user-attachments/assets/cb3c49ac-3a69-401f-8846-749bf5981555">

</details>

# Subneting
<details>

<summary>Subneting</summary>

## VLSM Topologi @ GNS3 
<img width="1500" alt="topo-gns" src="https://github.com/user-attachments/assets/dccfb792-bbad-43f7-93da-28b869dc8503">

</details>

## PEMBAGIAN IP
<img width="1500" alt="topo-gns" src="https://github.com/user-attachments/assets/12323a71-b037-4c56-b152-bd3033ff4998">

## NewEridu
```jsx
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
  address 192.244.0.1
  netmask 255.255.255.252
  
auto eth2
iface eth2 inet static
  address 192.244.0.5
  netmask 255.255.255.252

#A6
post-up route add -net 192.244.2.0 netmask 255.255.255.248 gw 192.244.0.2

#A3
post-up route add -net 192.244.0.8 netmask 255.255.255.248 gw 192.244.06

#A8
post-up route add -net 192.244.2.64 netmask 255.255.255.192 gw 192.244.0.2

#A7
post-up route add -net 192.244.2.8 netmask 255.255.255.248 gw 192.244.0.2

#A4
post-up route add -net 192.244.0.128 netmask 255.255.255.128 gw 192.244.0.6

#A5
post-up route add -net 192.244.1.0 netmask 255.255.255.0 gw 192.244.0.6

#A9
post-up route add -net 192.244.2.128 netmask 255.255.255.252 gw 192.244.0.2
```

## SixStreet (DHCP Relay)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.0.2
  netmask 255.255.255.252
  gateway 192.244.0.1

auto eth1
iface eth1 inet static
  address 192.244.2.1
  netmask 255.255.255.248

auto eth2
iface eth2 inet static
  address 192.244.2.9
  netmask 255.255.255.248

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A8
post-up route add -net 192.244.2.64 netmask 255.255.255.192 gw 192.244.2.3

#A9
post-up route add -net 192.244.2.128 netmask 255.255.255.252 gw 192.244.2.2

#A4
post-up route add -net 192.244.0.128 netmask 255.255.255.128 gw 192.244.0.1
```
## HDD (DNS)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.2.10
  netmask 255.255.255.248
  gateway 192.244.2.9

up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

## Fairy (DHCP)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.2.11
  netmask 255.255.255.248
  gateway 192.244.2.9

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A8
post-up route add -net 192.244.2.16 netmask 255.255.255.192 gw 192.244.2.9

#A4
post-up route add -net 192.244.0.128 netmask 255.255.255.128 gw 192.244.2.9
```

## OuterRing (DHCP Relay)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.2.3
  netmask 255.255.255.248
  gateway 192.244.2.1

auto eth1
iface eth1 inet static
  address 192.244.2.65
  netmask 255.255.255.192

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A9
post-up route add -net 192.244.2.128 netmask 255.255.255.252 gw 192.244.2.2

#A1
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.2.1

#A7
post-up route add -net 192.244.2.8 netmask 255.255.255.248 gw 192.244.2.1
```

## Burnice (Client)
```jsx
auto eth0
iface eth0 inet dhcp

#Hollowzero
post-up route add -net 192.244.2.128 netmask 255.255.255.252 gw 192.244.2.65

#A1
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.2.65
```

## Caesar (Client)
```jsx
auto eth0
iface eth0 inet dhcp

#Hollowzero
post-up route add -net 192.244.2.128 netmask 255.255.255.252 gw 192.244.2.65

#A1
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.2.65
```

## LuminaSquare (DCHP Relay)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.0.6
  netmask 255.255.255.252
  gateway 192.244.0.5

auto eth1
iface eth1 inet static
  address 192.244.0.9
  netmask 255.255.255.248
 
auto eth2
iface eth2 inet static
  address 192.244.1.1
  netmask 255.255.255.0

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A1
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.0.5

#A4
post-up route add -net 192.244.0.128 netmask 255.255.255.128 gw 192.244.0.11

#A7
post-up route add -net 192.244.2.8 netmask 255.255.255.248 gw 192.244.0.5
```

## Jane (Client)
```jsx
auto eth0
iface eth0 inet dhcp
```

## Policeboo (Client)
```jsx
auto eth0
iface eth0 inet dhcp
```

## HIA (Web Server)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.0.10
  netmask 255.255.255.248
  gateway 192.244.0.9
 
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

## HollowZero (Web Server)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.2.130
  netmask 255.255.255.252
  gateway 192.244.2.129

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A1
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.2.129
```

## BalletTwins (DHCP Relay)
```jsx
auto eth0
iface eth0 inet static
  address 192.244.0.11
  netmask 255.255.255.248
  gateway 192.244.0.9
 
auto eth1
iface eth1 inet static
  address 192.244.0.129
  netmask 255.255.255.128

up echo nameserver 192.168.122.1 > /etc/resolv.conf
 
#A2
post-up route add -net 192.244.0.4 netmask 255.255.255.252 gw 192.244.0.9

#A1
post-up route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.0.9

#A7
post-up  route add -net 192.244.2.8 netmask 255.255.255.248 gw 192.244.0.9
```

## Ellen (Client)
```jsx
auto eth0
iface eth0 inet dhcp 
```

## Lycaon (Client)
```jsx
auto eth0
iface eth0 inet dhcp 
```

## ScootOutpost
```jsx
auto eth0
iface eth0 inet static
  address 192.244.2.2
  netmask 255.255.255.248
  gateway 192.244.2.1

auto eth1
iface eth1 inet static
  address 192.244.2.129
  netmask 255.255.255.252

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A2
post-up route add -net 192.244.0.4 netmask 255.255.255.252 gw 192.244.2.1

#A8
post-up route add -net 192.244.2.16 netmask 255.255.255.192 gw 192.244.2.3

#A1
post-up  route add -net 192.244.0.0 netmask 255.255.255.252 gw 192.244.2.1
```

## Settingan Config
<details>

<summary>Detail Configure</summary>

# TUTORIAL
## PREREQUESITE

1. UDAH SUBNET DAN SUDAH ROUTING DAN UDAH BISA PING KE SEMUA NODES BARU LANJUT CONFIG 
2. Setup nameserver 192.168.122.1nya, masuk web console NewEridu trus run setup.sh
![alt text](images/image-10.png)

jangan lupa buat setiap nodes harus ada nameserver kyk dibawah ini
![alt text](images/image-11.png)

4. coba ping x.com dari NewEridu,SixStreet, OuterRing, Fairy
![alt text](images/image-12.png)
![alt text](images/image-14.png)
![alt text](images/image-13.png)
## CONFIG DHCP
Disini tutorial buat config DHCP 

1. Jangan lupa buat ganti IP di `isc-dhcp-relay` ini pake IP dari DHCP Server (Fairy)
untuk `isc-dhcp-relay` itu sama semua untuk OuterRing, SixStreet, LuminaSquare, BalletTwins
![alt text](images/image-77.png)
1. Copy config dari folder devices buat NewEridu, SixStreet, OuterRing, Fairy
2. Masuk ke web console Fairy trus run setup.sh
![alt text](images/image-2.png)

3. Masuk web console SixStreet trus run setup.sh trus biar pasti, run `service isc-dhcp-relay restart`
![alt text](images/image-3.png)


4. Masuk web console OuterRing trus run setup.sh trus biar pasti, run `service isc-dhcp-relay restart`
![alt text](images/image-4.png)
![alt text](images/image-15.png)


6. Coba masuk web console Fairy trus coba
`service isc-dhcp-server restart`
![alt text](images/image-6.png)
7. Coba restart clientnya, di stop trus start lagi misal si Caesar trus masuk web consolenya
![alt text](images/image-8.png)
trus coba liat juga di web console Fairy
`tail -f /var/log/syslog`
![alt text](images/image-9.png)
disini keliatan ada log ip 192.244.2.69 berhasil di lease ke Caesar
8. Kalo kyk gini udah bener berarti DHCPnya
buat DHCP client yang lain juga sama, relaynya direstart dulu, trus clientnya juga direstart (stop trus start) nanti bakal ada log lease sama kyk di caesar

## NO 2 FAIRY
1. web console Fairy trus cat setup.sh
copy yang command iptables paling bawah
![alt text](images/image-16.png)

2. cek iptables dulu (blom ada apa2)
![alt text](images/image-24.png)


3. run command ini
`iptables -A INPUT -p icmp --icmp-type echo-request -j DROP`
nanti dia bakal muncul di iptables
![alt text](images/image-78.png)

 4. fairy bisa ping ScootOutpost (192.244.2.129)
  ![alt text](images/image-22.png)

  tapi ScootOutpost gabisa ping fairy (192.244.2.11)
  ![alt text](images/image-23.png)

## NO 3 HDD
pasitiin HDD ini bisa ping ke semua nodes 

1. web console HDD trus run setup.sh

![alt text](images/image-25.png)

2. liat command iptables dipaling bawah
![alt text](images/image-26.png)

3. cek aturan sekarang (blom ada apa2) 
`iptables -L INPUT -n --line-numbers`
![alt text](images/image-27.png)

4. Bikin aturan untuk blok semua request 
`iptables -P INPUT DROP`
![alt text](images/image-28.png)

5. lalu buat aturan agar hanya Fairy (192.244.2.11) yang bisa akses
`iptables -A INPUT -s 192.244.2.11 -j ACCEPT`
![alt text](images/image-29.png)

6. 
fairy bisa ping ke HDD
![alt text](images/image-30.png)
tapi nodes lain gabisa ping ke HDD
![alt text](images/image-31.png)

7. test pake netcat 
di HDD nyalain netcat dlu baru yang lain
`nc -l -p 12345`
![alt text](images/image-45.png)
![alt text](images/image-48.png)
![alt text](images/image-46.png)
terlihat bahwa fairy bisa ping nc tapi yang lain gabisa ping nc

## NO 4 HollowZero
1. masuk web console HollowZero trus run setup.sh
![alt text](images/image-32.png)

2. trus cek buat nyoba webservernya
![alt text](images/image-50.png)

3. cek command iptables paling bawah
![alt text](images/image-34.png)

4. `date` buat liat tanggal sekarang, trus jalanin 3 command iptables dibawah
  ![alt text](images/image-35.png)

5. Caesar ga bisa ping ke HollowZero soalnya sekarang hari sabtu 
![alt text](images/image-36.png)

6. ganti aturan agar sabtu bisa diakses
![alt text](images/image-37.png)
drop aturan no 2 (yang 192.244.2.64 pokoknya)
`iptables -D INPUT 2`
`iptables -A INPUT -s 192.244.2.64/26 -m time --weekdays Sat -j ACCEPT`
kita allow hari sabtu
![alt text](images/image-38.png)

7. Caesar bisa ping dan curl ke HollowZero
![alt text](images/image-49.png)
## NO 5 HIA
1. web console HIA trus run setup.sh
![alt text](images/image-40.png)
2. cek buat nyoba webservernya
![alt text](images/image-52.png)
3. jalanin iptables dibawah
![alt text](images/image-42.png)
4. 
    a.  `iptables -P INPUT DROP`
    b. `iptables -A INPUT -s 192.244.0.128/25 -m time --timestart 08:00 --timestop 21:00 -j ACCEPT`
    c. `iptables -A INPUT -s 192.244.1.0/24 -m time --timestart 03:00 --timestop 23:00 -j ACCEPT`
![alt text](images/image-43.png)
5. Lycaon bisa akses karena sekarang masih masuk kedalam waktu yang diperbolehkan
![alt text](images/image-51.png)

## NO 6 HIA PORTSCAN
1. masuk web console HIA trus cat setup.sh
run iptables dari "Create a chain for handling port scanning" sampe bawah
![alt text](images/image-53.png)
2. cek web console policeboo trus ping sama curl ke HIA
![alt text](images/image-54.png)
![alt text](images/image-58.png)
masih bisa kan, coba kita nmap ke HIA
![alt text](images/image-55.png)
![alt text](images/image-56.png)
gabisa ping
![alt text](images/image-57.png)
curl jg gabisa

## NO 7 HollowZero
1. Masuk web console HollowZero trus cat setup.sh
![alt text](images/image-63.png)
run iptables yang bawah "Allow 2 active connections"
![alt text](images/image-64.png)
2. coba testing pake parallel di client bebas, antara Caesar, Burnice, Jane atau Policeboo
dan jangan lupa buat install parallel dulu
`apt update`
`apt install parallel -y`
![alt text](images/image-62.png)
untuk ip disini
`parallel curl -s IP_HOLLOWZER ::: IPCAESAR IPBURNICE IPJANE IPPOLICEBOO`
terlihat kalo hanya 2 koneksi yang bisa akses curl

## NO 8 Burnice

1. didalam setup.sh ada ip, itu IP dari HollowZero
2. masuk web console Burnice trus run setup.sh
![alt text](images/image-65.png)
cek juga ip dari burnice disini ipnya 192.244.2.67
liat di bagian inet
![alt text](images/image-67.png)
3. di hollowzero coba listen nc port 12345
`nc -l -p 12345`
![alt text](images/image-66.png)
4. di fairy kita netcat ke Burnice
![alt text](images/image-68.png)
5. nanti hollowzero yang akan mendapat messagenya bukan burnice
![alt text](images/image-69.png)

## MISI 3
1. sebelum meng isolasi Burnice kita disuruh kirim message ke Burnice
2. apt update
3. apt install netcat -y
4. nc -l -p 7777 
![alt text](images/image-73.png)
5. `iptables -F` buat clear rule iptables
5. kirim pesan ke burnice dari fairy
![alt text](images/image-72.png)
5. output di burnice
 ![alt text](images/image-71.png)

7. run iptables terakhir
![alt text](images/image-74.png)
![alt text](images/image-75.png)

8. test ping
![alt text](images/image-76.png)
gabisa di ping
selesai 


</details> 
