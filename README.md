# Samsara
Find all common user identification and permission needs in one place.

## Abstract

Samsara is a micro-service that aims to standardize and centralize user access control to embedded intranet applications.
You can easily install it in your infrastructure and set it up to make use of different authentication and authorization providers, exposing a user session through a common Hypermedia Protocol and easier to consume.

## Hypermedia API Sample

Creating a session

```
POST /sessions HTTP/1.0
Content-Type: application/json; charset=UTF-8

{"session":{"account":"guest","password":"1234","provider":"ldap"}}
```
```
HTTP/1.0 201 Created
Location: /session/1b5acd
```

Getting the created session

```
GET /session/1b5acd HTTP/1.0
Accept: application/json
Accept-Charset: UTF-8

{"session":{"account":"guest","provider":"ldap","name":"Guest User","email":"guest@email.info"}}
```
