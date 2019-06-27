# CS-APP

# CS-Backend
A simple backend for CS-APP.

Backend setup (backend directory)
You will need php and composer installed on your system.

1. Create a file named .env in the main directory with your database credentials. It should be identical to .env.example file.
    - Install all the things needed with:
    ``` composer install ```
    
2. Migrate the table for products to your database with:
    ``` php artisan migrate ```
    
3. Create some random entries with:
    ``` php artisan db:seed ```

4. Start the server with:
   ``` php -S localhost:8000 -t public ```

You can use the following routes:

GET /items <br/>
GET /item/{id} <br/>
POST /item <br/>
PUT /item/{id} <br/>
DELETE /item/{id} <br/>



# CS-Frontend

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# add axios manually 
npm i axios 

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
