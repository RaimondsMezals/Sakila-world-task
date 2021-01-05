# Sakila-world-task
Sakila task:
1
select first_name, last_name from actor;

2
select last_name from actor where first_name='JOHN';

3
select first_name, last_name from actor where last_name='NEESON';

4
SELECT first_name, last_name FROM actor WHERE actor_id % 10 = 0;

5
select description from film where film_id=100;

6
select title from film where rating='R';

7
select title from film where rating='R';

8
select title from film order by length asc limit 10;

9
select title from film order by length desc;

10
select title from film where special_features='Deleted Scenes';

11
select distinct last_name from actor having last_name is not null order by last_name desc;
/* I strugled with using "having" */

12
select last_name from actor group by last_name having count(last_name) > 1 order by count(last_name) desc;
/* Really dont like these 2 questions. */

13
select first_name, last_name from film_actor join actor_info on film_actor.actor_id=actor_info.actor_id group by film_actor.actor_id order by count(film_actor.actor_id) desc limit 1;

14
select release_year from film where title = 'Academy Dinosaur';

15
select avg(length) from film;

16
select category.name, avg(film.length) from category join film_category on film_category.category_id=category.category_id join film on film.film_id=film_category.category_id group by category.category_id order by avg(film.length) desc;

17
select title from film where description like '%robot%';

18
select count(release_year) as released_in_2010 from film where release_year=2010;

19
select film.title, category.name from category join film_category on film_category.category_id=category.category_id join film on film_category.film_id= film.film_id where category.name='Horror';

20
select first_name, last_name from staff where staff_id=2;

21
select film.title from film join film_actor on film_actor.film_id=film.film_id join actor on actor.actor_id=film_actor.actor_id where actor.first_name='Fred' and actor.last_name='Costner';

22
select distinct count(country) as distinct_countries from country;

23
select name from language order by name desc;

24
select first_name, last_name from actor where last_name like '%son' order by first_name asc;

25
select category.name as Most_popular_category from category join film_category on film_category.category_id=category.category_id group by category.category_id order by count(film_category.category_id) desc limit 1;
