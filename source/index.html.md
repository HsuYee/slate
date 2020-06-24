---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  # - shell
  # - ruby
  # - python
  # - javascript
  - json

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the Ai of Things API! 

# Authentication

> To authorize, use this code:


# Users

## Get All Users
This endpoint retrieves all users in array of JSON Object.

> User object structure:

```json
{
  "userid": "",
  "role": ""
}
```

### HTTP Request

`GET https://aiiot.southeastasia.cloudapp.azure.com/api/users`

<aside class="success">
Admin, Viewer
</aside>

## Update User
This endpoint will update user.

### HTTP Request

`POST https://aiiot.southeastasia.cloudapp.azure.com/api/user`

<aside class="success">
Admin
</aside>

## Delete User
This endpoint will delete user.

### HTTP Request

`DELETE https://aiiot.southeastasia.cloudapp.azure.com/api/user`

<aside class="success">
Admin
</aside>

# Permissions

## Get All Permissions
This endpoint retrieves all permissions in array of JSON Object.

> Permission object strcture:

```json
{
  "uri": "/api/devices",
  "method": "get",
  "roles": [
    "viewer",
    "admin"
  ],
  "ts": "2020-05-12T13:21:29.031Z"
}
```

### HTTP Request

`GET https://aiiot.southeastasia.cloudapp.azure.com/api/permissions`
<aside class="success">
Admin, Viewer
</aside>

# Contractors

## Get All Contractors
This endpoint retrieves all contractors in array of JSON Object.

> Contractor object structure:

```json
{
  "idnumber": "346789",
  "name": "user 2",
  "role": "cleaner",
  "countrycode": "+65",
  "mobilenumber": "91234521",
  "company": "Cleaning Service Pte Ltd",
  "escalatingnumber": "81231231",
  "smsgroups": "[\"sms group A\"]",
  "ts": "2020-05-21T07:01:22.130Z"
}
```

### HTTP Request

`GET https://aiiot.southeastasia.cloudapp.azure.com/api/permissions`
<aside class="success">
Admin, Viewer
</aside>

# Devices

## Get All Devices
This endpoint retrieves all devices in array of JSON Object.

> Device object structure:

```json
{
    "id": ,
    "deviceid": "",
    "serialno": "",
    "jsondata": {
      "tags": {
        "site": "",
        "block": "",
        "floor": "",
        "washroom": "",
        "subsystem": "",
        "alarmrules": [],
        "groupowner": "",
        "iotgateway": ""
      },
      "devicename": "",
      "devicelocation": []
    },
    "ts": ""
}
```

### HTTP Request

`GET https://aiiot.southeastasia.cloudapp.azure.com/api/devices`

<aside class="success">
Admin, Viewer
</aside>

## Device Control
### HTTP Request

`POST https://aiiot.southeastasia.cloudapp.azure.com/api/devicecontrol`

<aside class="success">
Viewer
</aside>

## Update Device
This endpoint will update device.

### HTTP Request

`POST https://aiiot.southeastasia.cloudapp.azure.com/api/device`

<aside class="success">
Admin
</aside>

## Delete Device
This endpoint will delete device.

### HTTP Request

`DELETE https://aiiot.southeastasia.cloudapp.azure.com/api/device`

<aside class="success">
Admin
</aside>


# Sensordata
## Sensordata
This endpoint retrieves all sensordata in array of JSON Object.

> Sensordata object structure:

```json
{
  "deviceid": "00158d0004089a4d",
  "status": true,
  "jsondata": [
    {
      "name": "temperature",
      "value": 27.49,
      "status": true
    },
    {
      "name": "humidity",
      "value": 53.18,
      "status": true
    }
  ],
  "alarms": [],
  "ts": "2020-06-24T17:36:06.464Z"
}
```

### HTTP Request

`POST https://aiiot.southeastasia.cloudapp.azure.com/api/sensordata`

<aside class="success">
Viewer
</aside>

## Latest Sensordata
### HTTP Request

`POST https://aiiot.southeastasia.cloudapp.azure.com/api/sensordatas/latest?num=:num&units=:units`

<aside class="success">
Viewer
</aside>

## Sensordata History

### HTTP Request

`GET https://aiiot.southeastasia.cloudapp.azure.com/api/sensordatas/history?num=:num&units=:units&deviceid=:deviceid`

<aside class="success">
Viewer
</aside>


# Categories

## Get All Categories
This endpoint retrieves all categories in array of JSON Object.

> Category object structure:

```json
{
  "id": 1,
  "tagname": "lightlocation",
  "jsondata": [
    {
      "id": "38cf7071-ce25-4c1e-a5c6-4a0a60f5252d",
      "name": "general office"
    },
    {
      "id": "54636c31-d031-4fa6-ae11-501bd55419fa",
      "name": "principle office"
    },
    {
      "id": "e95b4d49-8361-4d71-8761-3a24d65299c0",
      "name": "server room"
    }
  ],
  "multichoice": false,
  "protected": true,
  "useinfilter": false
}
```

### HTTP Request

`GET https://aiiot.southeastasia.cloudapp.azure.com/api/tags`

<aside class="success">
Admin, Viewer
</aside>

## Update Category
This endpoint will update category.

### HTTP Request

`POST https://aiiot.southeastasia.cloudapp.azure.com/api/tag`

<aside class="success">
Admin
</aside>

## Delete Category
This endpoint will delete category.

### HTTP Request

`DELETE https://aiiot.southeastasia.cloudapp.azure.com/api/tag`

<aside class="success">
Admin
</aside>

# Booter

## Get Booter
### HTTP Request

`GET https://aiiot.southeastasia.cloudapp.azure.com/api/booter`

<aside class="success">
Admin
</aside>

## POST Booter
### HTTP Request

`POST https://aiiot.southeastasia.cloudapp.azure.com/api/booter`

<aside class="success">
Admin
</aside>
