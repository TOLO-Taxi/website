---
layout: post
title: TOLO Partners
permalink: /integration/
---

### Build moving experiences through integration

Requesting a ride is easy with the TOLO API. Ride requests can be made once certain permissions are granted to your
registered app.

Our API lets you build services and solutions that make your customer experience more productive and rewarding. With our
API, you can place orders, get a driver assigned, receive realtime updates and more to shape the future of the on-demand
economy.

<a href="https://airtable.com/shrIy3caMLuwzsrj0" target="_blank">Apply here</a> to get permission start using our APIs.

## <a name="authorization" href="#authorization">#</a> Authorization

The HTTP request header `X-TOLO-ApiKey` should be used to provide credentials that authenticate a user agent with our
server, allowing access to all the protected services.

`X-TOLO-ApiKey=API_KEY`

**NOTE**: You will receive `API_KEY` upon approval of <a href="https://airtable.com/shrIy3caMLuwzsrj0" target="_blank">your application</a>


## <a name="profile" href="#profile">#</a> Get Your Profile

**Request**

`POST /api/me`

**Example Payload**

no payload is expected

**Sample Response**

```
{
  "user": {
    "api_key": "test_api_key",
    "average_rating": "4.8",
    "balance": "0",
    "country": "ET",
    "created_at": "2022-05-31 11:35:08.073224Z",
    "currency": "ETB",
    "email": "abebe@tolotaxi.com",
    "full_name": "Abebe Chala",
    "phone": "+251911000000",
    "phone_verified": true,
    "rating_tot_count": "129.0_27.0",
    "referrer_code": "",
    "token": "tYIxIIMECQcGZcJ-ciXE3u1jLSuxT",
    "version": "1.0.0+36"
  },
  "id": "fMSrm3azThKJsn-h3xAklX"
}
```

## <a name="create-order" href="#create-order">#</a> Create Order

**Request**

`POST /api/create-order`

**Example Payload**

```
{
 "pickup": {
   "latitude": 45.5328245,
   "longitude": 9.2256875
 },
 "destination": {
   "latitude": 45.472171,
   "longitude": 9.2051853
 },
 "service": "Taxi",
 "paymentMethod": "Cash"
}
```

**Sample Response**

```
{
 "status": "created",
 "orderId": "-N4OKnb16eaoX2iHd_GL"
}
```

## <a name="track-order" href="#track-order">#</a> Track Order

**Request**

`GET /api/order/:orderId`

**Example Payload**

no payload is expected

**Sample Response**

```
{
  ...
  "service": "Taxi",
  "destination_address": "Bole Medhanialem",
  "driver_location": {
    "latitude": "45.5413479",
    "longitude": "9.2334028"
  },
  "driver_name": "Abebe Kebede",
  "driver_phone": "+251911000000",
  "payment_method": "Cash",
  "pickup_address": "Meskel Sqaure", 
  "status": "ended",
}
```