# Docker haqida ma'lumotlar o'zbek tilida

> **Docker** — bu dasturlarni konteynerlarda ishga tushirish uchun foydalaniladigan ochiq kodli platforma. Docker
> yordamida dasturlarni barcha kerakli kutubxonalar va bog'liqliklar bilan birga qadoqlab, turli muhitlarda bir xil
> ishlashini ta'minlash mumkin

## Docker Asosiy buyruqlar

#### `🔰`Docker versiasini bilish

    docker -v

___

#### `📄`Docker haqida butun tizim ma'lumotlari ko'rish

    docker info

___

#### `🔰`Docker accuntga kirishw

    docker login

___

#### `🔰`Docker accountdan chiqish

    docker logout

___

#### Docker HUB dan image qidirish uchun quidagi buyruqdan foylanish mumkin

    docker search image_name

___

#### Docker HUBdagi image yuklab olish uchun

    docker pull image_name

___

#

## 🗃 CONTAINER HAQIDA QISQACHA

> **Docker Container** - Bu Docker Image asosida ishlaydigan izolaysiyalangan muhitdir. Har bir kontenyer o'z operatsion
> tizim kutubxonalari va bo'gliqliklari bilan birga keldi.

#### Dockerda 2 xil commandlar mavjud bular

1. __Management command__
2. __Commands__

 ___

#### `🔶`Docker container ro'yxatini ko'rish kodi

    docker container ls -a

___

#### `♻` Docker image va container o'rtasidagi farq

* __image bu darturimiz filelar__
* __container image ishlab turgan xolati Yani ishlab turgan image bu CONTAINER__

___

#### `🔰`Kiritilgan image Yaratadi va ishga tushurish uchun

    docker container run image_name

___

#### Containerni qayta ishga tushurish uchun

    docker restart container_id

___

#### `✅` To'xtab turgan containerni ishga tushurish kodi quidagicha 👇

    docker container start container_id

___

#### `🛑`Ishlab turgan containerni to'xtatishni 2 xil usuli mavjud

1.     docker container stop container_id
2.     docker container kill container_id 

___

#### `🔰` Containerga ulanish uchun quidagicha buyruq berish lozim! 👇

    docker container attach container_id

___ 

#### `❌` Containerni o'chirishsh buyrug'i quidagicha 👇

    docker container rm kontainer_id

___

#### 🔠 Barcha ishlamayotgan containerlarni o'chirish uchun quidagicha buyruqdan foyadalanish kerak

    docker container prune

___

#### Docker containerdagi loglarni korish uchun

    docker logs container_id

___

#

## IMAGE haqida

> **Docker Images** - Bu docker containerlarni yaratish uchun ishlatiladigan statik andozalar. Ular dastur va uning
> barcha bog'liqliklarining o'z ichiga oladi. Docker images Docker HUB yoki boshqa Docker registerlaridan yuklanishi
> mumkin

#### `🔰` Imageni ishga tushurish quidagicha

    docker image run image_name

___

#### `❌` Imageni faqaat bittasini o'chirish quidagicha

    docker image rmi image_name

___

#### `❌` Barcha ishlamayotgan imagelarni ochirish uchun

    docker image prune

___

#### `🔶` Imagelar royxatini korish uchun

    docker images

___

#

## Volumes haqida

> **Docker Volumes (Xotira hajmi)** - kontaynerda ishlatiladigan malumotlarni saqlash va boshqarish uchun ishlatiladi.
> Kontaynerlar odatda **efemeral (muddati cheklangan)** boladi. Yani kontayber ochganda yoki qayta ishga tushurilganda
> malumotlar yoqoladi. Docker Volumes esa **malumotlarni uzoq mudatli** saqlash imkonini beradi.

> **Docker Volumes-ni asosiy maqsadi** - Konteynerlarning **o'zgaruvchan malumotlarini saqlash** va konteynerlar **o'rtasida
umumiy malumotlarni ulashishdir**

> **Docker Volumes asosiy xususiyatlari**
> 1. Persistent Storage (Doimiy xotira)
>    * Volumes yordamida saqlangan ma'lumotlar konteyner o‘chirilgandan so‘ng ham saqlanadi.
> 2. Data Sharing (Ma'lumot ulashish)
> 3. Backup and Restore (Zaxira nusxalarini olish va tiklash)
> 4. Performance (Ishlash tezligi)


#### Barcha volumelar royxati

    docker volume ls

#### Volume yaratish

    docker volume create volume_name

#### Volumeni bittasini o'chirish

    docker volume rm volume_name

#### Barcha Volumlarni ochirish uchun

    docker volume prune

*** 

#

## 🌐 Docker NETWORKING haqida

> **Docker tarmog'ida 3 asosiy tarmoq turi mavjud**
> 1. **Bridge Network (Ko'plik tarmo'gi)**
>      * Bu Docker-da yaratilgan asosiy tarmoq turi
>      * Ushbu tarmoq turi **Default bridge** deb ham ataladi.
>      * Konteynerlar faqat bir xil hostda bo‘lganda bir-biri bilan aloqa qila oladi.
> 2. **Host Network (Host tarmo'gi)**
>      * Bu tarmoq turi konteynerlarni Docker host tarmog‘iga bevosita ulaydi.
>      * u tarmoqda konteynerlar hostning IP-manzilini va portlarini ishlatadi.
>      * Konteynerlar bir xil hostda joylashgan barcha xizmatlar bilan bevosita aloqa o‘rnatishi mumkin.
> 3. **Overlay Network (Overlay tarmog‘i)**
>      * Bu tarmoq turi Docker swarm yoki Docker Enterprise-da foydalaniladi.
>      * Bir nechta Docker hostlari orasida tarqalgan konteynerlarni ulaydi.
>      * Bu tarmoq distributed environment (taqsimlangan muhit) uchun juda foydali.
___

#### Barcha `Networking` ro'yxati

    docker network ls

---

#### `Networking` yaratish

    docker network create network_name

---

#### `Networking` bittasini o'chirish

    docker neteork rm network_name

---

#### Barcha `Networkinglarni` o'chirish

    docker network prune

#

## 🐋 Docker-Compose

> **Docker Compose** - Bu bir nechta docker konteynerlarni birgalikda boshqarish uchun ishlatiladigan vosita.
> **Docker Compose** yordamida bir nechta xizmatlarni bitta konfiguratsiya fayli yordamida sozlash va ishga tushurish
> mumkin


#### Docker-compose fileni ishga tushurish

    docker-compose up

---

#### Docker-compose ish faoliyani to'xtatish

    docker-compose down

---

#### Docker-composelar ro'yxatini korish

    docker-compose ps
