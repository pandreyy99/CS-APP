# CS-APP

# CS-Backend
A simple backend for CS-APP(RESTful API developed with Lumen).

Backend setup (backend directory)
You will need php and composer installed on your system.

However, if you are not using Homestead, you will need to make sure your server meets the following requirements: <br/>

***PHP >= 7.1.3*** <br/>
***OpenSSL PHP Extension*** <br/>
***PDO PHP Extension*** <br/>
***Mbstring PHP Extension*** <br/>

You can run this script in order to find if you have these 3 extensions installed :

```
    <?php
    if(!extension_loaded('openssl')) {
        throw new Exception('This app needs the Open SSL PHP extension.');
	}
    else echo 'Open SSL PHP extension installed!'. PHP_EOL , "<br>";

    if (!defined('PDO::ATTR_DRIVER_NAME')) {
	    echo 'PDO PHP unavailable';
	}
    else echo 'PDO PHP extension installed!'. PHP_EOL , "<br>";

    if (!extension_loaded('mbstring')) { 
	    echo 'Mbstring PHP extension not found!';
	}
    else echo 'Mbstring PHP extension installed!'. PHP_EOL, "<br>";	
	?>
```

1. Create a file named .env in the main directory with your database credentials. It should be identical to .env.example file.
    - Run the following command in your terminal to create a new project with Lumen:
    ``` composer create-project --prefer-dist laravel/lumen items ```
    
2. Migrate the table for items to your database with:
    ``` 
        php artisan make:migration create_items_table
        php artisan migrate
    ```
    
3. Create some random entries with:
    ``` php artisan db:seed ```

4. Start the server with:
   ``` php -S localhost:8000 -t public ```

You can use the following routes:

Get all items - ***GET /api/items*** <br/>
Get one item - ***GET /api/items/{id}*** <br/>
Create an item - ***POST /api/items*** <br/>
Edit an item - ***PUT /api/items/{id}*** <br/>
Delete an item - ***DELETE /api/items/{id}*** <br/>

**Note:** *You'll need MySQL. Navigate to the mysql website and install the community server edition. If you are using a Mac, I'll recommend following these instructions. To avoid micromanaging from the terminal, I'll also recommend installing a MySQL GUI, Sequel Pro.*

For detailed information go to [Lumen documentation](https://lumen.laravel.com/docs/5.8).

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
