# Node JS ADS API Doc

URL: https://adlisting.herokuapp.com

## Auth API

**How to Register new user?**

`POST /register`

Input

```
{
  "name":"sundar",
  "email":"sundar@appmaking.co",
  "password": "123456"
}
```

**How to login?**

`POST /login`

Input

```
{
  "email":"sundar@appmaking.co",
  "password": "123456"
}
```

## Ads API

**How to fetch all ads?**

```
GET /ads
```

It doesnot requires any input in body or header

**How to create new ad?**

```
POST /ads
```

Input (body): 
```
{
    "title": "iPhone for sale",
    "description": "Good Condition",
    "price": 20000,
    "mobile": "+919500707757",
    "images":[
      "uploads/file.jpg",
      "uploads/file1.jpg",
    ]
}
```
This POST method requires authorization (Bearer). so you need to pass your JWT token inside header.

**How to fetch ads for logged user?**

```
POST /ads/user
```

This POST method requires authorization (Bearer). so you need to pass your JWT token inside header.

**How to update ad?**

```
PATCH /ads
```

Input:

```
{
    "title": "iPhone for sale",
    "description": "Good Condition",
    "price": 20000,
    "mobile": "+919500707757",
    "images":[
      "uploads/file.jpg",
      "uploads/file1.jpg",
    ]
}
```
This PATCH method requires authorization (Bearer). so you need to pass your JWT token inside header.


**How to delete ad?**

```
DELETE /ads/:id
```

This DELETE method requires authorization (Bearer). so you need to pass your JWT token inside header.


## Uploads API

You need to upload file as a multipart/form-data

**How to upload single image**

```
POST /upload/picture
```

Input name: avatar

**How to upload multiple images?**

```
POST /upload/photos
```

Input name: photos

