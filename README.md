# Домашнее задание к занятию «Работа с данными (DDL/DML)»- Старцев Данила Антонович

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

---

Задание можно выполнить как в любом IDE, так и в командной строке.

### Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.
>![1.1](https://github.com/MindMaze74/sql_ddl/blob/main/img/1.png)
1.2. Создайте учётную запись sys_temp.
1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)
>![1.3](https://github.com/MindMaze74/sql_ddl/blob/main/img/2.png)
1.4. Дайте все права для пользователя sys_temp.
1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
>![1.5](https://github.com/MindMaze74/sql_ddl/blob/main/img/3.png)
1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос: 
```sql
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
>![смена](https://github.com/MindMaze74/sql_ddl/blob/main/img/4.png)

1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.
1.7. Восстановите дамп в базу данных.
>![1.6-1.7](https://github.com/MindMaze74/sql_ddl/blob/main/img/5.png)
1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
>![1.8](https://github.com/MindMaze74/sql_ddl/blob/main/img/6.png)
*Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.*


### Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)
```
+----------------------------+
| Tables_in_sakila           |
+----------------------------+
| actor                      |
| actor_info                 |
| address                    |
| category                   |
| city                       |
| country                    |
| customer                   |
| customer_list              |
| film                       |
| film_actor                 |
| film_category              |
| film_list                  |
| film_text                  |
| inventory                  |
| language                   |
| nicer_but_slower_film_list |
| payment                    |
| rental                     |
| sales_by_film_category     |
| sales_by_store             |
| staff                      |
| staff_list                 |
| store                      |
+----------------------------+|

+---------------+--------------+
| TABLE_NAME    | COLUMN_NAME  |
+---------------+--------------+
| actor         | actor_id     |
| address       | address_id   |
| category      | category_id  |
| city          | city_id      |
| country       | country_id   |
| customer      | customer_id  |
| film          | film_id      |
| film_actor    | actor_id     |
| film_actor    | film_id      |
| film_category | film_id      |
| film_category | category_id  |
| film_text     | film_id      |
| inventory     | inventory_id |
| language      | language_id  |
| payment       | payment_id   |
| rental        | rental_id    |
| staff         | staff_id     |
| store         | store_id     |
+---------------+--------------+
```
>![2](https://github.com/MindMaze74/sql_ddl/blob/main/img/7.png)

## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.

### Задание 3*
3.1. Уберите у пользователя sys_temp права на внесение, изменение и удаление данных из базы sakila.

3.2. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
>![3.2](https://github.com/MindMaze74/sql_ddl/blob/main/img/8.png)
*Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.*

### Команды которые использовались при выполнении задания

**Запуск контейнера MySQL 8.0 (Docker)**
```bash
docker run --name mysql8 -e MYSQL_ROOT_PASSWORD=rootpass -d -p 3306:3306 mysql:8.0
```

**Подключение к MySQL внутри контейнера (для выполнения SQL-команд)**
```bash
docker exec -it mysql8 mysql -u root -p
```

**Команды, относящиеся к Заданию 1**
```bash
CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'password';
```

 **Список пользователей**
 ```bash
SELECT User, Host FROM mysql.user;
```

**Выдача всех прав**
 ```bash
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

**Проверка прав**
 ```bash
SHOW GRANTS FOR 'sys_temp'@'localhost';
```
**Смена типа аутентификации**
 ```bash
ALTER USER 'sys_temp'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```

**Восстановление дампа Sakila**
```bash
wget https://downloads.mysql.com/docs/sakila-db.zip
unzip sakila-db.zip
docker cp sakila-db/sakila-schema.sql mysql8:/tmp/
docker cp sakila-db/sakila-data.sql mysql8:/tmp/
```
**Внутри MySQL**
```bash
SOURCE /tmp/sakila-schema.sql;
SOURCE /tmp/sakila-data.sql;
```
**Получение списка таблиц базы**
```bash
USE sakila;
SHOW TABLES;
```
**Команды для Задания 2 через DBeaver**
```bash
SELECT 
    TABLE_NAME AS 'Название таблицы',
    GROUP_CONCAT(COLUMN_NAME ORDER BY ORDINAL_POSITION SEPARATOR ', ') AS 'Название первичного ключа'
FROM
    INFORMATION_SCHEMA.KEY_COLUMN_USAGE
WHERE
    TABLE_SCHEMA = 'sakila'
    AND CONSTRAINT_NAME = 'PRIMARY'
GROUP BY TABLE_NAME
ORDER BY TABLE_NAME;
```

**Команды для Задания 3**
```bash
REVOKE INSERT, UPDATE, DELETE ON sakila.* FROM 'sys_temp'@'localhost';
FLUSH PRIVILEGES;
```
**Проверка прав после отзыва**
```bash
SHOW GRANTS FOR 'sys_temp'@'localhost';
```
**Запуск DBeaver и настройка подключения**
```bash
cd ~/Downloads
tar -xzf dbeaver-ce-26.1.1-linux-x86_64.tar.gz
sudo mv dbeaver /opt/
/opt/dbeaver/dbeaver
```
**Настройки подключения в DBeaver:**
```
Host: 127.0.0.1
Port: 3306
User: root
Password: rootpass
Дополнительные свойства: allowPublicKeyRetrieval=true, useSSL=false
```
