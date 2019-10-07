
# G10卒業制作メモ

名前の通り

## CentOS

root    -> s2KhJ7P3
webapp  -> i5heDk74

## Mysql

root -> hOeh6?7gH

car_program -> Dehi8d=C

---

- table list
    - car_table
    - point_table
    - log_table
    - send_table

## SQLMemo

SQLのメモだよ

### car_table

~~~SQL
CREATE TABLE car_table
(
    ID SMALLINT ZEROFILL AUTO_INCREMENT,
    name VARCHAR(10) UNIQUE,
    PRIMARY KEY(ID)
);

### point_table
~~~SQL
CREATE TABLE point_table
(
    ID SMALLINT ZEROFILL AUTO_INCREMENT,
    name VARCHAR(10) UNIQUE,
    PRIMARY KEY(ID)
);
~~~

### log_table

~~~SQL
/*いうても未定*/
CREATE TABLE log_table
(
    ID SMALLINT ZEROFILL AUTO_INCREMENT,
    sonar_val FLOAT NOT NULL,
    gyro_val FLOAT NOT NULL,
    dc_val FLOAT NOT NULL,
    sarvo_val FLOAT NOT NULL,
    battery_bal FLOAT NOT NULL,
    PRIMARY KEY(ID)
)
~~~

### send_table

~~~SQL
CREATE TABLE send_table(
    ID SMALLINT ZEROFILL AUTO_INCREMENT,
    send_time TIME NOT NULL,
    car_id SMALLINT FOREIGN KEY(car_id) REFERENCES car_table(ID),
    log_id SMALLINT FOREIGN KEY(log_id) REFERENCES log_table(ID),
    point_id SMALLINT FOREIGN KEY(point_id) REFERENCES point_table(ID),
)
~~~
