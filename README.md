# week05
#1. 使用 INSERT 指令新增一筆資料到 user 資料表中，這筆資料的 username 和 password 欄位必須是 ply。接著繼續新增至少 4 筆隨意的資料。
mysql> insert into user(name,username,password,time) values('josh','ply','ply',now());
Query OK, 1 row affected (0.00 sec)

mysql> insert into user(name,username,password,time) values('jason','123','1234',now());
Query OK, 1 row affected (0.00 sec)

mysql> insert into user(name,username,password,time) values('endiva','ply','1234',now());
Query OK, 1 row affected (0.00 sec)

mysql> insert into user(name,username,password,time) values('ken','ply','ply',now());
Query OK, 1 row affected (0.01 sec)

mysql> insert into user(name,username,password,time) values('Rui','456','144',now());
Query OK, 1 row affected (0.00 sec)

mysql> insert into user(name,username,password,time) values('mike','13','13',now());
Query OK, 1 row affected (0.00 sec)

#2.使用 SELECT 指令取得所有在 user 資料表中的使用者資料。
select * from user;

<img width="483" alt="截圖 2021-03-24 下午10 15 12" src="https://user-images.githubusercontent.com/76401750/112325164-69cbc880-8cee-11eb-8160-3aed4154277d.png">

#3.使用 SELECT 指令取得 user 資料表中總共有幾筆資料。
select count(id) from user;

<img width="353" alt="截圖 2021-03-24 下午10 16 41" src="https://user-images.githubusercontent.com/76401750/112325394-9da6ee00-8cee-11eb-9e53-f02f52b044c3.png">

#4.使用 SELECT 指令取得所有在 user 資料表中的使用者資料，並按照 time 欄位，由近到遠排序。
select * from user order by time desc;

<img width="448" alt="截圖 2021-03-24 下午10 19 39" src="https://user-images.githubusercontent.com/76401750/112325901-08582980-8cef-11eb-9463-ed23e86d2bec.png">

#5.使用 SELECT 指令取得 user 資料表中第 2 ~ 4 共三筆資料，並按照 time 欄位，由近到遠排序。
select * from user where (id>1 and id<5) order by time desc;

<img width="503" alt="截圖 2021-03-24 下午10 23 12" src="https://user-images.githubusercontent.com/76401750/112326481-86b4cb80-8cef-11eb-9ddc-624217162620.png">

#6.使用 SELECT 指令取得欄位 username 是 ply 的使用者資料。
select * from user where username='ply';

<img width="473" alt="截圖 2021-03-24 下午10 25 57" src="https://user-images.githubusercontent.com/76401750/112326904-e9a66280-8cef-11eb-9b1d-e64253f87460.png">

#7.使用 SELECT 指令取得欄位 username 是 ply、且欄位 password 也是 ply 的資料。
select * from user where username='ply' and password='ply';

<img width="512" alt="截圖 2021-03-24 下午10 26 53" src="https://user-images.githubusercontent.com/76401750/112327046-0cd11200-8cf0-11eb-82b2-f521fc2c4767.png">

#8.使用 UPDATE 指令更新欄位 username 是 ply 的使用者資料，將資料中的 name 欄位改成【丁滿】。
update user set username='丁滿' where username='ply';
select * from user;

<img width="485" alt="截圖 2021-03-24 下午10 29 25" src="https://user-images.githubusercontent.com/76401750/112327444-65081400-8cf0-11eb-9a9f-3036b5edd025.png">


#9.使用 DELETE 指令刪除所有在 user 資料表中的資料。
delete from user;
select * from user;

<img width="343" alt="截圖 2021-03-24 下午10 31 13" src="https://user-images.githubusercontent.com/76401750/112327722-a5679200-8cf0-11eb-9e52-81c73f5667bf.png">




