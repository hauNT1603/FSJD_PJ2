# API Endpoint List

### User
[Aster mark meaning this API need JWT token]

-  Index  (GET `/users`) *
-  Show  (GET `/users/:id`) *
-  Create  (POST `/users`) *
-  Update  (PUT `/users/:id`) *
-  Delete  (DELETE `/users/:id`) *

### Product

-  Index (GET `/products`)  
-  Show (GET `/products/:id`)
-  Create  (POST `/products`) *
-  Update  (PUT `/products/:id`) *
-  Delete  (DELETE `/products/:id`) *

### Order

-  Index  (GET `/order`) *
-  Show  (GET `/order/:id`) *
-  Current Order by user (args: user id) (GET `/order/current-order/:id`) *
-  Create order(POST `/order/`)
-  Create order by id(POST `/order/add-to-order/:id`) *
-  Update (PUT `/order/:id`) *
-  Delete (DELETE `/order/:id`) *

# Data Schema

### User

```sql
CREATE TABLE users (
  id              BIGSERIAL PRIMARY KEY,
  username        VARCHAR(250) NOT NULL,
  firstname       VARCHAR(250) NOT NULL,
  lastname        VARCHAR(250) NOT NULL,
  password_digest VARCHAR(250) NOT NULL
);
```

### Product

```sql

CREATE TABLE products (
  id    BIGSERIAL PRIMARY KEY,
  name  VARCHAR(250) NOT NULL,
  price INTEGER      NOT NULL,
  description text
);
```

### Order

```sql
CREATE TABLE orders (
  id      BIGSERIAL PRIMARY KEY,
  user_id INTEGER NOT NULL REFERENCES users (id),
  status  BOOLEAN NOT NULL
);
```

### Order_Product

```sql
CREATE TABLE order_products (
  order_id   INTEGER NOT NULL REFERENCES orders (id),
  product_id INTEGER NOT NULL REFERENCES products (id),
  quantity   INTEGER NOT NULL
);
```
