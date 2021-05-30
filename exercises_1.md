# TESTING OUT THE FIELD #

"There's a guy screaming at the top of his lungs non stop with a microphone and speaker, he acts like he's singing but he's just howling... this is NYC!"

1. 
`ALTER TABLE famous_people
RENAME TO celebrities;`

2.
```sql
ALTER TABLE celebrities
RENAME COLUMN name TO first_name;

ALTER TABLE celebrities
ALTER COLUMN first_name varchar(80);
```

3. 
```sql
ALTER TABLE celebrities
ADD COLUMN last_name varchar(100);
#ALTER TABLE
#forgot to to set to NOT NULL therefore
ALTER TABLE celebrities
ALTER COLUMN last_name SET NOT NULL;
#ALTER TABLE
```

4.
```sql
ALTER TABLE celebrities
ALTER COLUMN date_of_birth TYPE date
USING date_of_birth::date
ALTER COLUMN date_of_birth SET NOT NULL;
```

5.
```sql
ALTER TABLE animals
ALTER COLUMN max_weight_kg TYPE decimal(10,4);
```

6.
```sql
ALTER TABLE animals
ADD CONSTRAINT unique_binomial_name UNIQUE (binomial_name);
```

7.
```sql
\c ls_burgers

\d orders

ALTER TABLE orders
ADD COLUMN customer_email varchar(50),
ADD COLUMN customer_loyalty_points integer DEFAULT 0;
```

8.
```sql
ALTER TABLE orders
ADD COLUMN burger_cost decimal(4,2) DEFAULT 0,
ADD COLUMN side_cost decimal(4,2) DEFAULT 0,
ADD COLUMN drink_cost decimal(4,2) DEFAULT 0;
```

9.
```sql
ALTER TABLE orders
DROP COLUMN order_total;
```

`test`















