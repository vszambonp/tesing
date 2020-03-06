# REST API GUIDE

## To start the project, do:

``` 
$ cd [root directory]
$ composer install
$ sudo php -S localhost:8000
```

## Routes

HTTP Method | Route
------------ | -------------
POST | auth/login
POST | auth/logout
GET | customers
POST | customers
PUT | customers
DELETE | customers/{id}

## How to use

   1. POST auth/login
   
   Before using anny of other routes, first you have to authenticate yourself as a user. For this you must
   post the following for this route:
   
      ``` 
           {
	            "email":"vszambon@gmail.com",
	            "password":"1234"
            }
      ```


