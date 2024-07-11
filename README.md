# Docker haqida ma'lumotlar o'zbek tilida

## Docker Asosiy buyruqlar

### `🔰`Docker versiasini bilish

    docker -v

___

### `📄`Docker haqida butun tizim ma'lumotlari ko'rish

    docker info

___

### `🔰`Docker accuntga kirishw

    docker login

___

### `🔰`Docker accountdan chiqish

    docker logout

___

### Docker HUB dan image qidirish uchun quidagi buyruqdan foylanish mumkin

    docker search image_name

___

### Docker HUBdagi image yuklab olish uchun

    docker pull image_name

___

###            

## 🗃 CONTAINER HAQIDA QISQACHA

___

### Dockerda 2 xil commandlar mavjud bular

1. __Management command__
2. __Commands__

 ___

### `🔶`Docker container ro'yxatini ko'rish kodi

    docker container ls -a

___

### `♻` Docker image va container o'rtasidagi farq

* __image bu darturimiz filelar__
* __container image ishlab turgan xolati Yani ishlab turgan image bu CONTAINER__

___

### `🔰`Kiritilgan image Yaratadi va ishga tushurish uchun

    docker container run image_name

___

### Containerni qayta ishga tushurish uchun

    docker restart container_id

___

### `✅` To'xtab turgan containerni ishga tushurish kodi quidagicha 👇

    docker container start container_id

___

### `🛑`Ishlab turgan containerni to'xtatishni 2 xil usuli mavjud

1.     docker container stop container_id
2.     docker container kill container_id 

___

### `🔰` Containerga ulanish uchun quidagicha buyruq berish lozim! 👇

    docker container attach container_id

___ 

### `❌` Containerni o'chirishsh buyrug'i quidagicha 👇

    docker container rm kontainer_id

___

### 🔠 Barcha ishlamayotgan containerlarni o'chirish uchun quidagicha buyruqdan foyadalanish kerak

    docker container prune

___

### Docker containerdagi loglarni korish uchun

    docker logs container_id

___

## IMAGE haqida

___

### `🔰` Imageni ishga tushurish quidagicha

    docker image run image_name

___

### `❌` Imageni faqaat bittasini o'chirish quidagicha

    docker image rm -f image_name

___

### `❌` Barcha ishlamayotgan imagelarni ochirish uchun

    docker image prune

___

### `🔶` Imagelar royxatini korish uchun

    docker image ls