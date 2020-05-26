
## table - person
1. 
create table person (
id serial primary key,
  name text,
  age int,
  height int,
  city text,
  favorite_color text
);

2.
insert into person(
  favorite_color,
  city,
  height,
  age,
  name
 )
 values (
  'green',
  'dallas',
  168,
  24,
  'bob'
 );

 insert into person(
  favorite_color,
  city,
  height,
  age,
  name
 )
 values(
   'red',
   'phoenix',
   189,
   25,
   'lilly'
  );

  insert into person(
  favorite_color,
  city,
  height,
  age,
  name
 )
 values(
   'blue',
   'ocean side',
   111,
   29,
   'billy'
  );

  insert into person(
  favorite_color,
  city,
  height,
  age,
  name
 )
 values(
   'pink',
   'new york city',
   154,
   21,
   'cait'
  );

insert into person(
  favorite_color,
  city,
  height,
  age,
  name
 )
 values(
   'black',
   'tucson',
   186,
   27,
   'tausif'
  );

3.
  select * from person
  order by height desc
;

4.
select * from person
  order by height asc
;

5.
select * from person
  order by age desc
;

6.
select * from person
  where age > 20
;

7.
select * from person
where age = 18;

8. 
select * from person
where age < 20 or age >30;

9.
select * from person
where age != 27;

10.
select * from person
where favorite_color != 'red';

11.
select * from person
where favorite_color != 'red' and 
favorite_color != 'blue';

12.
select * from person
where favorite_color = 'green' or 
favorite_color = 'orange';

13.
select * from person
where favorite_color in (
  'orange', 'green', 'blue'
);

14.
select * from person
where favorite_color in (
  'yellow', 'purple'
 );


## table - orders
1.
create table orders(
  order_id serial primary key,
  person_id int,
  product_name text,
  product_price int,
  quantity int
 );

2.
insert into orders(
  product_price,
  quantity,
  person_id,
  product_name
 )
 values(
   13,
   4,
   123,
   'chicken'
);

 insert into orders(
  product_price,
  quantity,
  person_id,
  product_name
 )
 values(
   14,
   5,
  456,
   'steak'
);


insert into orders(
  product_price,
  quantity,
  person_id,
  product_name
 )
 values(
   10,
   1,
  789,
   'hamburger'
);

 insert into orders(
  product_price,
  quantity,
  person_id,
  product_name
 )
 values(
   5,
   3,
  726,
   'fries'
);

insert into orders(
  product_price,
  quantity,
  person_id,
  product_name
 )
 values(
   2,
   1,
  074,
   'water'
);

3.
select * from orders;

4.
select sum(quantity) from orders;

5.
select sum(product_price * quantity) from orders;

6.
select sum(product_price * quantity) from orders
where person_id = 123;

## table - artist
1.
insert into artist(
  name
 )
 values(
   'caitlin'
);

 insert into artist(
  name
 )
 values(
   'tausif'
);

 insert into artist(
  name
 )
 values(
   'jc'
);

2.
select * from artist
order by name desc limit 10;

3.
select * from artist
order by name asc limit 5;

4.
select * from artist
where name like 'Black%';

5.
select * from artist
where name like '%Black%';

## table - employee

1.
select first_name, last_name from employee
where city = 'Calagry'

2.
select max(birth_date) from employee;

3.
select min(birth_date) from employee;

4.
select * from employee
where reports_to = 2;

5.
select count(*) from employee 
where city = 'Lethbridge'

## table - invoice

1.
select count(*) from invoice
where billing_country = 'USA';

2.
select max(total) from invoice;

3.
select min(total) from invoice;

4.
select * from invoice 
where total > 5;

5. 
select count(*) from invoice
where total < 5;

6.
select count(*) from invoice 
where billing_state in ('CA', 'TX', 'AZ');

7.
select avg(total) from invoice;

8.
select sum(total) from invoice;