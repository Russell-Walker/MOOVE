# MOOVE

Ниже приведены команды для каждого из перечисленных заданий:

1)  получение всех имен и фамилий людей в определенном кабинете

SELECT DISTINCT first_name, last_name, room FROM optimized.staff WHERE room = '539';
2) добавление нового телефона сотруднику

INSERT INTO optimized.staff(department, email, first_name, last_name, phone, position, room) 
VALUES('Clerical Office', 'William_Anderson@example.com', 'William', 'Anderson','+75649310000', 'Specialist' , '5424');
3) получение списка телефонов всех сотрудников определенной должности в одном из отделов;

SELECT first_name, last_name, phone, position, department FROM optimized.staff WHERE position = 'Manager' AND department = 'Clerical Office';
4) добавление нового сотрудника

INSERT INTO optimized.staff(department, email, first_name, last_name, phone, position, room) 
VALUES('Clerical Office', 'Ivan_ivanov@example.com', 'Ivan', 'Ivanov','+70649310000', 'Specialist' , '5424');
5) перемещение сотрудника в другой отдел со сменой комнаты

UPDATE optimized.staff SET department = 'Sales', room='42' WHERE first_name = 'William' AND last_name = 'Anderson';

CSV таблицу можно было оптимизировать в базу данных с несколькими родственными таблицами (Relative tables) для удобства, однако, я еще не разобрался как это сделать.
