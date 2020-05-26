### Лабораторная работа №2

Выполнил: Назаров Александр Олегович ББСО-01-18:
##### Задание 1
По заданию я выбрал соответствующие характеристики для виртуалки:
![screen](https://psv4.userapi.com/c856324/u145451303/docs/d14/2b4363a6bf8c/1.jpg?extra=7MaPDDuPavXdRcVZNsojk-HFKqEOr1jJlqhCp_gXpuri9H7kvzPz0LfS8ejx4YuplNnsHemyADPEK7CRz3HU--iZUxgH8yy7aKX1SzqsNDAFBuQrNTFRkb-XljYW1aOhPsGVcjtja2J1Audy8nOhdyiDmQ)

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d4/7fee7438e705/2.jpg?extra=z_CsHQKY6gxMMF3N5Ztf5eEH4Iz4xKBnrm0Rvx0yJTRFCrCk9hkU4sSZ6EHTQUeqEgB_voAZpoYt45dPoLPsLj5OdfhtVBodMRcpf0EjQ97g0MnXH3WQJ4SLJdjS_s35f1j0gWCg0YLnU5_rxxeMeJQ-Gg)

Потом приступил к ручной разметке:
![screen](https://psv4.userapi.com/c856324/u145451303/docs/d11/2471c2d500c9/4.jpg?extra=dnR94lR_6ovcd8AMOhLGErfvCFWrIaAzDhWjGKruUy5D2CbSVayBOak4nUSf4cvbipKBkCQyCgJoJ5Y3OPCPFTVbgLEivl3Iwpzx82mO5SGkchNeQ4fDpNayrywAZmgITdSXmHRPMUjw0Ig32ohfVBcv0w)


Создал разметкупод raid:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d8/f249d7fa990e/5.jpg?extra=-SFicrmUBRwagxlIz-8FlWa0ry8VnC-lbtLewA_oROk3UTbnFTLNwJfmdMJOZWhpYEcOFFLIgca_A0kbqOEakK_b0LLiXeOsGy4Ga_Yo1gId-89chmMmt44XB5KipPAAe-2yVbtJLOwEY7yLCPI0nN78Xg)


Создал RAID1:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d15/2f62dfc632e6/6.jpg?extra=FM2DzaznpQH9LMK9nPiogysxva8xWzPWuf9E_Tmejr2JXilwIMxp1m2EKh9NFKa4TwDqIIAkIbgvNDEzYEpzWs2-b66PtyCt5js6bLQNt9ZS-47NxEpRWC25K90KWCXKn-QLEG0JjJOHbk9_ex4oLFq1Eg)



Создал группу томов LVM:


![screen](https://psv4.userapi.com/c856324/u145451303/docs/d6/6b3e9b02fe17/7.jpg?extra=QfmGPUxbxK2ZboBQuhiLB3j8xxJOCpYTDH7sNZobGTc8N4F1vCWTnO7V27OcMMfMaInB4PBeBQW3M64A7pLLOfAlaivkXPoUqN36jYfZMNDoTVLMdKRzGLntKMikie03ElP5v3w_BY6b3lZdWate8E039w)



Установил томам LVM точки монтирования:



![screen](https://psv4.userapi.com/c856324/u145451303/docs/d6/1179b2c04996/8.jpg?extra=lYX_JlunzyFN5yjSP1cKfkClkFZdOR81t4EOIdkknOhpFURrp-OPIUXZq14v_f06nTSboGoq2cZhckTBgnwMQ5P71yiCNf6KUE6oD8op5258EUcSuqqvW00AeJN57QF30fJNrg_7g9zDEvjO8oOH_D8OcQ)


Далее установил GRUB на sda:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d15/0497a5368872/9.jpg?extra=HeZP7b5Wqrt1LWrqqYwlvz8vmVv7BRSLdfecO20-M_kYybcFpfTwf7YsHgimKe-RrXvEfpKEpLTCqQ3Sp7i9A-HNfkFwtU-GtQXL-M6lkCJSzSW5G2xUcjW0VXfR27n2HlPq1aOModSalFwcjtUpSEwbDw)

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d16/85deb7e65abf/10.jpg?extra=tKecFk4TBGn7h2Y7Kn85vEXgGetl_6r8XjxDALqcR-7BN6YEZ-wa7V-EfJS7QwFwvhEjmDQtt9Wdm4SzGgN_1Kq0YBW3u46DmXj9AePXipwUWHXhN3YLHPwYF9LJGeH9UJpiffHQuYt0gkYAh15AstpyJQ)

Всё работает:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d1/6216423a7320/20.jpg?extra=BcNFoIGhfG7I_KAXNZHNR0dHmc76vfGPA8SciEocxSeS_jYk5LTe2S_003Q6yOpIfTZnmogWksUDKITBKWTTwTJ8xcr0J6zoU6wtrRt6e-51ragbOkYt99Kialz8m11TrkJh16Tfcu1GE2uUYSEnRsq7LQ)


С помощью lsblk посмотрел информацию о состоянии дисков. С помощью команды dd if=/dev/sda1 of=/dev/sdb1 я копировал содержимое раздела /boot с диска sda (ssd1) на диск sdb (ssd2). Выполнил установку загрузчика ОС на второй диск с помощью grub-install /dev/sdb. Теперь в случае отказа первого диска система сможет спокойно загрузится:


![screen](https://psv4.userapi.com/c856324/u145451303/docs/d18/ff749d339638/12.jpg?extra=maAiwsBfCyOMzyGXcp6n5ON07wE79nlW5xLSIsOqK553x0MIOE8gtzJGA3wAXjqvEetu__v_LqEcVGr3KmzSYUww9Gdpep2Hiq0OhCk5IicHTWcnJH4V1i9Bru12I4gfVLvay_wyFFht5yClQss_1NgoiQ)

C помощью cat /proc/mdstat я увидел состояние raid, где md0 — имя RAID устройства; raid1 sda2[0] sdb2[1] — из каких дисков собран; 1046528 blocks — размер массива; [2/2] [UU] — количество юнитов, которые на данный момент используются:
pvs - выводит информацию о физической памяти:
lvs - выводит информацию о Logical Volume:
vgs - выводит информацию о группе томов LVM:
![screen](https://psv4.userapi.com/c856324/u145451303/docs/d10/83c3569dd513/13.jpg?extra=ivv3saD6-8BmWvBi_9I4qyrOgNLlIFPHFLgnikT4gJ_I4icc2ff3bY6CCJ2rDcHE3vwteULQNVQr77Hq21QFU0Q4jmSTN7FYtH7v17ASqmhajkbJc0egh0XJrUkc_7SlwhlwdqHLQo-WETopHW4Php_NpA)

##### Задание 2
Команда fdisk -l после удаления диска ssd1 показала следующее:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d9/ac025f6ae771/15.jpg?extra=6pQWYNY5HzWevGCdwkPWS6Ano0nAime_mE1LxICXT08icT9Q945bDFBbYnVSDAPPXelQVLL_KT95t2Ci7VTiWlNqt2AwEoAAIj34pbex8HsL7S-StyPWpSDwiQyvGYXzX1pQdGMD_o58EyJXTB8ny8GIrA)

Cоздал новый диск. Cистема его видит. Скопировал таблицу разделов со старого диска на новый с помощью sfdisk -d /dev/sda | sfdisk /dev/sdb и добавил новый диск в наш raid c помощью команды mdadm --manage /dev/md0 --add /dev/sdb2. Получил:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d9/dc826ea0b830/16.jpg?extra=2IAm8yPMfVKNVaujJNZBgWLRgugG91Agw5VKCmPn_mm6pb-rNVAooFSLsqgDcYqtJ_hocyFPiQukb7y2JodMX_N3hJVcH-0dvwhR5I0fJR1KkC_I9Ak5xmKrOe3UmprE0QgvFi5bB8oE2YZYuGP1fI9Ohg)
![screen](https://psv4.userapi.com/c856324/u145451303/docs/d1/a86bd4ec653a/17.jpg?extra=DCfqBzHyGEuTBlJ-3l8EOjr0KZCKnJqAP4mEcPT7FIj9VD5R-LE6GXwX5BrEFyERgE6nMt486lZ546TknH9DmhKZ-VW7BqebXpZrs2b09vV7G5ZCjhrdv68So-n5xhoGjozVtEY0uVZGzl3a6ueVMYtFSg)

После установил GRUB и копировал раздел в /boot 


![screen](https://psv4.userapi.com/c856324/u145451303/docs/d2/d80d065fe2a5/19.jpg?extra=a65zwsacSZdKtTQ790yiNEJ5GwBWZa9qVidSPHTtfF3am4cVfP42uK9UVht-8gDfEG0wdRV3KL6rS-nM7LW8CA16cXNNChlNlmDRuDQf0DKXdXNAJULVWrGcWfN24Qflh-sQ80jBmfrW5lHmIzA--wbSPw)

##### Задание №3

Проэмулировал отказ диска ssd2, удалив его из свойств ВМ:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d2/d80d065fe2a5/19.jpg?extra=a65zwsacSZdKtTQ790yiNEJ5GwBWZa9qVidSPHTtfF3am4cVfP42uK9UVht-8gDfEG0wdRV3KL6rS-nM7LW8CA16cXNNChlNlmDRuDQf0DKXdXNAJULVWrGcWfN24Qflh-sQ80jBmfrW5lHmIzA--wbSPw)

Добавил один новый ssd диск, назвав его ssd4:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d4/db353535fab1/20.jpg?extra=tf51UDp33fw684o9GR0W7Jq1F1EpaiwnYrYQNfw4-cc3VzALB8dqjWCDPbCCtdzDJ0CCJrxdQ-bKKbcidoOhCxBbkRjhcupFoMJ-NZvqW9iwuPRaw_eukjZePCd41Yz_6kn7jOiaIOzwWjvpPvsFHn1TVw)

Копирую файловую таблицу со старого диска на новый: sfdisk -d /dev/sda | sfdisk /dev/sdb:
![screen](https://psv4.userapi.com/c856324/u145451303/docs/d5/97fcaa54f4ff/21.jpg?extra=MWkiPKR96BQ2_kZy-yoVm_3UqcW36IJFqBhC_JMceTdblxRj2YzhTyCfA5q2JDV3DTT_fi8NIchDSOWFs5zXFgHNIYBWddAYu1YepCr3N9_vhePvJYlZVIXX3RMHbbPorOMuuR0O9SowgNzAF-xyZCsZxQ)


Выполним команду lsblk -o NAME,SIZE,FSTYPE,TYPE,MOUNTPOINT и затем с помощью команды dd скопируем данные /boot на новый диск :

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d11/9aec457dbcf6/22.jpg?extra=pv8o7yLT_xFLoebv2wZLrisPeMqegIVvLFMNtoeZ8Z-x4on1tBzKybXi8eWNBwo7OKHfmJycZdaswA8z_xLnRokHaaO3GHbgw2Fg6uL-kmio5GT47PPcm1MWAxUhUD8whJTBZcbyd7VFPmtObf_n-Dx2UA)


Устанавливаю загрузчик на новый диск sdb: grub-install /dev/sdb . Далее создаем новый рейд-массив(mdadm --create --verbose /dev/md63 --level=1 --raid-devices=1 /dev/sdb2. В итоге у нас установлен новый RAID-массив md63, проверяем при помощи команды cat /proc/mdstat:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d8/424c5719d780/23.jpg?extra=ymqOFtpedQyG3BMKxHQgXTHntb6BCLNroNNuG_noJb5a3o6Bu8cocmfHDwaxFc0fqnDWxuVmrvG5JDNB8_cuNldSVvEVse6mN6jwo8EV6RTITJoC-mLDKK0pmZiJQHnueudLAjpzwXr2M25-SMTo7-BdVA)


Настраиваем LVM:
Создаём новый физический том, включив в него ранее созданный RAID-массив: pvcreate /dev/md63 и проверяем командой lsblk -o NAME,SIZE,FSTYPE,TYPE,MOUNTPOINT:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d4/d596f1183d8d/24.jpg?extra=527mTMTpg2iqfYniGLX5X-KfcBw583smJwtoWh9JyIc_YlWHxB4AorHmYrjwZoPPZxi7FBGY2AJYANHbZzIE0fsCZvNM1v0Oq35hDIsWaqzgLErmQ8MgktKZ-5qlW-pGc_4tXVTqVG5xrR0C3KfqwCjECQ)


LV var,log,root находятся на диске sda:

![screen](https://psv4.userapi.com/c856324/u145451303/docs/d15/7303271a654c/25.jpg?extra=Rr-aoln9JlP0o3B7Uv-BHeutN-uQcymLRDCiKde21dqwh9t3Hw-y8hK6eWw-4LHeYO1SQbd2gOldRa2Wpk-yzM1ldsK7fQqkydjCsa7Zd56AUROVuLe6VdaFzVgfNM45xAMUxpq33Rzy3tsqmC9yaQ96Vw)


Выполняю перемещение данных со старого диска на новый, не получается. Пришлось заново поставить систему и провести все операции

![screen](screens/27.png)


Видно, что данные находятся на одном диске:  
  
![screen](screens/28.png)  
  
Изменил Volume Group, удалив из него диск старого raid и также проверякм, что раздел /boot не пустой :  
  
![screen](screens/29.png)  
  
Проверим, что произошло после добавления дисков (диски появились):  
  
![screen](screens/30.png)  
  
Когда мы скопировали таблицу разделов со старого диска оказалось, что новый размер не использует весь объем жесткого диска:  
  
![screen](screens/31.png)  
  
Cкопируем загрузочный раздел /boot с диска ssd4 на ssd5 `dd if=/dev/sda1 of=/dev/sdb1` и установим grub на новый диск (ssd5):  
  
![screen](screens/32.png)  
  
Сначала изменили размер второго раздела диска ssd5 (sdb), затем перечитали таблицу разделов и провели результат:  
  
![screen](screens/33.png)   
  
Добавляем новый диск к текущему RAID-массиву, расширяем количество дисков в нашем массиве до 2-х штук.  
  
![screen](screens/34.png)  
  
Сначала увеличили размер раздела на диске ssd4 (sda), а затем перечитали таблицу разделов и проверили результат:  
  
![screen](screens/35.png)   
  
Получили sda2 и sdb2 разделы, которые имеют размер > чем размер RAID-устройство.  
  
Расширяем размер RAID   
  
![screen](screens/36.png)   
  
![screen](screens/37.png)  


Увеличили объём памяти ssd4, ssd5.  
  
Завершили миграцию основного массива на новые диски, работа с ssd4 и ssd5 закончена.  
  
![screen](screens/38.png)   

Перемещаем `/var/log` на новые диски, для этого создаем новый RAID-массив, создаём логический том:  
  
![screen](screens/39.png) 

Перетащил данные логов со старого раздела на новый:  
  
![screen](screens/40.png)   
  
Редактирую /etc/fstab fstab - файл, в котором записываются правила, по которым при загрузке будут смонтированы разделы (поправляю устройство 'system-log' на 'data-var_log') и затем используем команду resize2fs для изменения ФС:
  
![screen](screens/41.png)  
  
Выполним перезагрузку, а затем проверку, что сделано всё, что хотели:   
Завершили установку:   
  
![screen](screens/42.png)   
  
Завершили установку.  

В итоге за эту лабораторную я создал виртуалку с двумя дисками, настроил работу ЛВМ, провел имитацию аварии диска, заменил диск на лету и перенёс разделы.
