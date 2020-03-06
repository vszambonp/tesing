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
   post the following JSON for this route:
   
      ``` 
           {
	            "email":"vszambon@gmail.com",
	            "password":"1234"
            }
      ```
      
   2 . POST auth/logout
   
   Send this post request to logout the user from the system.
   
   3 . GET customers
   
   List all customers contacts from the logged user. It'll return an array of customer in the following JSON formar:
   
   ```
   	{
            "firstname": "Vitor",
            "lastname": "Zambon",
            "email": "asdf@gmail.com",
            "phones": [
                {
                    "number": "123123123123",
                    "id": "1"
                },
                {
                    "number": "432143214132",
                    "id": "2"
                }
            ],
            "braddress": {
                "cep": "14160710",
                "logradouro": "Rua Y",
                "complemento": null,
                "bairro": "Centro",
                "localidade": "Sertãozinho",
                "uf": "SP",
                "a_id": "4"
            },
            "user_id": "1",
            "c_id": "56"
        }
```
   
   3 . POST customers
   
   Insert new customer for logged user. For this you must post the following JSON structure for this route:
   
    ``` 
       {
            "firstname": "Vitor",
            "lastname": "Zambon",
            "email": "vszambon@gmail.com",
            "phones": [
	    	{
			"number":"123123123123"
		},
	    	{
			"number":"432143214132"
		}
	    ],
            "braddress": {
                "cep": "14160710",
                "logradouro": "Rua Y",
                "complemento": "apto X",
                "bairro": "Centro",
                "localidade": "Sertãozinho",
                "uf": "SP"
            }
        }
    ```
   3 . PUT customers
   
   To update a customer. For this you must post the following JSON structure for this route:
   
    ``` 
        {
            "firstname": "Vitor",
            "lastname": "Zambon",
            "email": "asdf@gmail.com",
            "phones": [
                {
                    "number": "123123123123",
                    "id": "1"
                },
                {
                    "number": "432143214132",
                    "id": "2"
                }
            ],
            "braddress": {
                "cep": "14160710",
                "logradouro": "Rua Y",
                "complemento": null,
                "bairro": "Centro",
                "localidade": "Sertãozinho",
                "uf": "SP",
                "a_id": "4"
            },
            "user_id": "1",
            "c_id": "56"
        }
    ```
   
  

