# SQLinNode.js_connect-to-db-in-code

💻Список сотрудников#
Получать список сотрудников для планирования дней рождений из базы данных.

💻 API списка задач#
Реализовать элементарный CRUD для API списка задач.

Install#
sudo apt update
sudo apt install postgresql postgresql-contrib
Usage#
sudo -u postgres psql # connect to db using system user postgres
New user and database#
В командном интерфейсе psql (заменить <username>, <database_name> и пароль на то, что вам надо):

Создать пользователя:

create user <username>;
Включить для пользователя доступ по паролю:

alter user <username> with encrypted password '<password>';
Дать пользователю вся права на работу с новой базой данных <database_name>:

grant all privileges on database <database_name> to <username>;
Подключаемся новым пользователем:

postgres -h 127.0.0.1 <database_name> <username>
Не забываем заменить имя пользователя и базы. К примеру, у вас получиться:

postgres -h 127.0.0.1 todolist todolist_app
CAUTION
Когда не указан host сервера, сервер пустит пользователя только если его имя в ОС соответствует тому, к которому вы подключаетесь. Это настройка в файле pg_hba.conf (пример полного пути для PostgreSQL версии 10 /etc/postgresql/10/main/pg_hba.conf). Что бы ее "обойти" надо явно указать host. За это в примере выше отвечает параметр -h 127.0.0.1.

💻 Работы с таблицами psql#

 Создать и наполнить таблицу со списком сотрудников (дня планирования дней рождения)
 Создать и наполнить таблицу для списка задач
