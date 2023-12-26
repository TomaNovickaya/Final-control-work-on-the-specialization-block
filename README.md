Итоговая контрольная работа
Новицкая Т.А.


Информация о проекте
Необходимо организовать систему учета для питомника в котором живут домашние и вьючные животные.


Как сдавать проект
Для сдачи проекта необходимо создать отдельный общедоступный репозиторий(Github, gitlub, или Bitbucket). Разработку вести в этом репозитории, использовать пул реквесты на изменения. Программа должна запускаться и работать, ошибок при выполнении программы быть не должно. Программа, может использоваться в различных системах, поэтому необходимо разработать класс в виде конструктора
Задание
1.	Используя команду cat в терминале операционной системы Linux, создать два файла Домашние животные (заполнив файл собаками, кошками, хомяками)
tamara@tamara-linux:~$ cat>'Домашние животные' Собаки Кошки Хомяки  и Вьючные животными заполнив файл Лошадьми, верблюдами и ослы), 
tamara@tamara-linux:~$ cat>'Вьючные животные' Лошади Верблюды Ослы
а затем объединить их. 
tamara@tamara-linux:~$ cat 'Домашние животные' 'Вьючные животные'>'Все животные'
Просмотреть содержимое созданного файла. 
tamara@tamara-linux:~$ cat 'Все животные' Переименовать файл, дав ему новое имя (Друзья человека).
tamara@tamara-linux:~$ mv 'Все животные' 'Друзья человека'
![1](https://github.com/TomaNovickaya/Final-control-work-on-the-specialization-block/assets/126395023/94a07632-dfcb-4ff0-90c0-998c3d945df8)

2.	Создать директорию, переместить файл туда.
 tamara@tamara-linux:~$ mkdir final  tamara@tamara-linux:~$ mv 'Друзья человека' final 
 


3.	Подключить дополнительный репозиторий MySQL. Установить любой пакет из этого репозитория.
tamara@tamara-linux:~$ wget https://dev.mysql.com/get/mysql-apt-config_0.8.24-1_all.deb  tamara@tamara-linux:~$ sudo dpkg -i mysql-apt-config_0.8.24-1_all.deb  tamara@tamara-linux:~$ sudo apt-get update  tamara@tamara-linux:~$ sudo apt-get install mysql-server  tamara@tamara-linux:~$ systemctl status mysql   
 
4.	Установить и удалить deb-пакет с помощью dpkg.
tamara@tamara-linux:~$ wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-j_8.0.32-1ubuntu22.04_all.deb  tamara@tamara-linux:~$ sudo dpkg -i mysql-connector-j_8.0.32-1ubuntu22.04_all.deb tamara@tamara-linux:~$ sudo dpkg -r mysql-connector-j 
 
 

 

5.	Выложить историю команд в терминале ubuntu
 

6.	Нарисовать диаграмму, в которой есть класс родительский класс, домашние животные и вьючные животные, в составы которых в случае домашних животных войдут классы: собаки, кошки, хомяки, а в класс вьючные животные войдут: Лошади, верблюды и ослы).

 

7.	В подключенном MySQL репозитории создать базу данных “Друзья человека”
CREATE DATABASE  human_friends;
8.	Создать таблицы с иерархией из диаграммы в БД

USE  human_friends;
CREATE TABLE `human_friends`.`dogs` (
  `idDogs` INT NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(45) NOT NULL,
  `datebirth` DATE NOT NULL,
  `commands` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`idDogs`));

CREATE TABLE `human_friends`.`cats` (
  `idcats` INT NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(45) NOT NULL,
  `datebirth` DATE NOT NULL,
  `commands` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`idcats`));

CREATE TABLE `human_friends`.`hamsters` (
  `idhamsters` INT NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(45) NOT NULL,
  `datebirth` DATE NOT NULL,
  `commands` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`idhamsters`));

CREATE TABLE `human_friends`.`horses` (
  `idhorses` INT NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(45) NOT NULL,
  `datebirth` DATE NOT NULL,
  `commands` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`idhorses`));

CREATE TABLE `human_friends`.`camels` (
  `idcamels` INT NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(45) NOT NULL,
  `datebirth` DATE NOT NULL,
  `commands` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`idcamels`));

CREATE TABLE `human_friends`.`donkeys` (
  `iddonkeys` INT NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(45) NOT NULL,
  `datebirth` DATE NOT NULL,
  `commands` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`iddonkeys`));

9.	Заполнить низкоуровневые таблицы именами(животных), командами которые они выполняют и датами рождения
INSERT INTO `human_friends`.`camels` (`name`, `datebirth`, `commands`) VALUES ('Agata', '13.01.2000', 'spit');
INSERT INTO `human_friends`.`camels` (`name`, `datebirth`, `commands`) VALUES ('Ida', '01.05.2021', 'spit');
INSERT INTO `human_friends`.`camels` (`name`, `datebirth`, `commands`) VALUES ('Vasya', '13.11.2022', 'spit');
INSERT INTO `human_friends`.`camels` (`name`, `datebirth`, `commands`) VALUES ('Jared', '05.05.2013', 'spit');

INSERT INTO `human_friends`.`cats` (`name`, `datebirth`, `commands`) VALUES ('Iriska', '01.02.2010', 'Meow, scratching');
INSERT INTO `human_friends`.`cats` (`name`, `datebirth`, `commands`) VALUES ('Samuil', '03.05.2022', 'Meow, jump');
INSERT INTO `human_friends`.`cats` (`name`, `datebirth`, `commands`) VALUES ('Tatka', '07.11.2021', 'Meow');
INSERT INTO `human_friends`.`cats` (`name`, `datebirth`, `commands`) VALUES ('Sting', '11.11.2015', 'Meow, licking');

INSERT INTO `human_friends`.`dogs` (`name`, `datebirth`, `commands`) VALUES ('Juja', '11.12.2021', 'Bark');
INSERT INTO `human_friends`.`dogs` (`name`, `datebirth`, `commands`) VALUES ('Veles', '05.05.2020', 'Bark, jump');
INSERT INTO `human_friends`.`dogs` (`name`, `datebirth`, `commands`) VALUES ('Baddy', '07.03.2023', 'Jump, tumbling');
INSERT INTO `human_friends`.`dogs` (`name`, `datebirth`, `commands`) VALUES ('Chara', '06.11.2015', 'Bark');

INSERT INTO `human_friends`.`donkeys` (`name`, `datebirth`, `commands`) VALUES ('Lary', '15.11.2020', 'Shout');
INSERT INTO `human_friends`.`donkeys` (`name`, `datebirth`, `commands`) VALUES ('Blakky', '01.03.2023', 'Shout, plowing');

INSERT INTO `human_friends`.`hamsters` (`name`, `datebirth`, `commands`) VALUES ('Homka', '13.07.2022', 'Nibble');
INSERT INTO `human_friends`.`hamsters` (`name`, `datebirth`, `commands`) VALUES ('Pushok', '01.03.2018', 'Nibbleб stock up');
INSERT INTO `human_friends`.`hamsters` (`name`, `datebirth`, `commands`) VALUES ('Funtick', '03.04.2023', 'Nibble');

INSERT INTO `human_friends`.`horses` (`name`, `datebirth`, `commands`) VALUES ('Yagodka', '13.02.2023', 'Plowing');
INSERT INTO `human_friends`.`horses` (`name`, `datebirth`, `commands`) VALUES ('Boi', '12.01.2020', 'Plowing, pull, mow');
INSERT INTO `human_friends`.`horses` (`name`, `datebirth`, `commands`) VALUES ('Merlin', '02.03.2015', 'Plowing, pull, mow');
INSERT INTO `human_friends`.`horses` (`name`, `datebirth`, `commands`) VALUES ('Kamelia', '15.02.2018', 'Plowing, pull, mow');
10.	Удалив из таблицы верблюдов, т.к. верблюдов решили перевезти в другой питомник на зимовку. Объединить таблицы лошади, и ослы в одну таблицу.
DROP TABLE camels;
SELECT *FROM donkeys CROSS JOIN horses;
11.	Создать новую таблицу “молодые животные” в которую попадут все животные старше 1 года, но младше 3 лет и в отдельном столбце с точностью до месяца подсчитать возраст животных в новой таблице
CREATE TABLE `human_friends`.`young_animals` (
  `idyoung_animals` INT NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(45) NOT NULL,
  `datebitrh` DATE NOT NULL,
  `commands` VARCHAR(100) NOT NULL,
  `age` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`idyoung_animals`));

SELECT *FROM cats WHERE datebirth <= '2022-12-26' AND datebirth >= '2020-12-26';
12.	Объединить все таблицы в одну, при этом сохраняя поля, указывающие на прошлую принадлежность к старым таблицам.
SELECT *FROM cats, dogs, hamsters, horses CROSS JOIN young_animals;
