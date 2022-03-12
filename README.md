# SQL-SELF-JOIN



create table tabemploye(employe_id int not null identity,name varchar(50),manager_id int)

insert into tabemploye(name,manager_id) values ('ashish',null), ('shweta',1), ('lavi',null), ('vimal',3), ('naman',2)

update tabemploye set manager_id=4 where employe_id = 3

select * from tabemploye

------------------------------------inner self join-----------------------------------------------

select * from tabemploye E inner join tabemploye M on E.manager_id = M.employe_id

-----------------------------------left self join---------------------------------

select * from tabemploye E left join tabemploye M on E.manager_id = M.employe_id

-----------------------------------right self join----------------------------------

select * from tabemploye E right join tabemploye M on E.manager_id = M.employe_id

-------------------------------full self join------------------------------------------

select * from tabemploye E full join tabemploye M on E.manager_id = M.employe_id

-------------------------------cross self join-----------------------------------

select * from tabemploye E cross join tabemploye M
