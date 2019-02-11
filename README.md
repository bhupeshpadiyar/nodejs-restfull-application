# nodejs-restfull-application
Simple RESTFULL CRUD services developed with nodejs

## Steps to run the project
1. Download/Clone The Project
2. Go to the project folder
3. Run following commands to run the application
      ```
      npm install
      ```
      ```
      npm index
      ```
      or
      
      ```
      noidemon index
      ```
      
## Create Contact Service
Request Type - POST 
Request URL :
```
http://localhost:8080/api/contacts
```
Request Body :
```
{
	"name": "Bhupesh Singh",
	"email": "bhupesh@gmail.com",
	"gende": "male",
	"phone": "1234567890"
}
```

Response - 
```
{
    "message": "New contact created!",
    "data": {
        "_id": "5c60fa2f33bd0439ee89bff9",
        "create_date": "2019-02-11T04:29:35.691Z",
        "name": "Bhupesh Singh",
        "email": "bhupesh@gmail.com",
        "phone": "1234567890",
        "__v": 0
    }
}
```

## Read Contact By Id Service
Request Type - GET 
Request URL :

```
http://localhost:8080/api/contacts/5c60fa2f33bd0439ee89bff9
```


Response: 
```
{
    "message": "Contact details loading..",
    "data": {
        "_id": "5c60fa2f33bd0439ee89bff9",
        "create_date": "2019-02-11T04:29:35.691Z",
        "name": "Bhupesh Singh",
        "email": "bhupesh@gmail.com",
        "phone": "1234567890",
        "__v": 0
      }
}
```

## Read All Contacts Service
Request Type - GET 
Request URL :

```
http://localhost:8080/api/contcats
```

Response: 

```
{
    "status": "success",
    "message": "Contacts retrieved successfully",
    "data": [
        {
            "_id": "5c60f3949b233f37d9803266",
            "create_date": "2019-02-11T04:01:24.953Z",
            "name": "Bhupesh Singh Padiyar",
            "gender": "MALE",
            "email": "bhupeshsingh@gmail.com",
            "phone": "1234567890",
            "__v": 0
        },
        {
            "_id": "5c60fa2f33bd0439ee89bff9",
            "create_date": "2019-02-11T04:29:35.691Z",
            "name": "Bhupesh Singh",
            "email": "bhupesh@gmail.com",
            "phone": "1234567890",
            "__v": 0
        }
    ]
}
```

## Delete a Contact Service
Request Type - DELETE 
Request URL :

```
http://localhost:8080/api/contacts/5c60f3949b233f37d9803266
```

Response: 

```
{
    "status": "success",
    "message": "Contact deleted"
}
```

## Update Contact Service
Request Type - PUT 
Request URL :

```
http://localhost:8080/api/contacts/5c60f3e09b233f37d9803267
```

Request:

```
{
	"name": "Bhupesh Singh Padiyar",
	"email": "bhupesh@gmail.com",
	"gende": "male",
	"phone": "0123456789"
}
```

Response: 

```
{
    "message": "Contact Info updated",
    "data": {
        "_id": "5c60f3e09b233f37d9803267",
        "create_date": "2019-02-11T04:02:40.431Z",
        "name": "Bhupesh Singh Padiyar",
        "email": "bhupesh@gmail.com",
        "phone": "0123456789",
        "__v": 0
    }
}
```
