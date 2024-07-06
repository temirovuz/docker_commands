# Docker haqida ma'lumotlar o'zbek tilida

### Dockerda 2 xil commandlar mavjud bular

1. __Management command__
2. __Commands__

 ___

### 🔶Docker container ro'yxatini ko'rish kodi

        docker container ls -a

___

### ♻ Docker image va container o'rtasidagi farq

* __image bu darturimiz filelar__
* __container image ishlab turgan xolati Yani ishlab turgan image bu CONTAINER__

___

### ✅To'xtab turgan containerni ishga tushurish kodi quidagicha 👇

        docker container start container_name

___

### 🛑Ishlab turgan containerni to'xtatishni 2 xil usuli mavjud

1.      docker container stop container_name
2.      docker container kill container_name 

___

### 🔰 Containerga ulanish uchun quidagicha buyruq berish lozim! 👇

        docker container attach container_name

___ 

### ❌ Containerni ochish buyrug'i quidagicha 👇

        docker continer rm kontainer_name

___
### 🔠 Barcha ishlamayotgan containerlarni ochirish uchun quidagicha buyruqdan foyadalanish kerak
    docker container prune