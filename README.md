# TIXID-API
Unofficial TIX-ID API

Last tested on TIX-ID version 1.11.0

## Get Token
All this route is using Auth Bearer `<token>` except this route, and token is can be found from this route
#### POST https://api.tix.id/v1/token
Add `Client-Secret` key to Header with value `123456`

  ##### Response
  ![image](https://user-images.githubusercontent.com/16686825/49083212-94242d00-f27e-11e8-9ae9-cc7561c25389.png)
  That token will be used for <code>Authorization Bearer</code>
## Get App Config
#### GET https://api.tix.id/v1/app_config
  ##### Response
  ![image](https://user-images.githubusercontent.com/16686825/49084280-8de38000-f281-11e8-82e0-405d9ac00526.png)
 
## Promo Banner
#### GET https://api.tix.id/v1/content/promo/banner
  ##### Reponse
  ![image](https://user-images.githubusercontent.com/16686825/49084466-195d1100-f282-11e8-82a3-b80607be9f8d.png)

## Cities ID
#### GET https://api.tix.id/v1/cities
  ##### Response
  ![image](https://user-images.githubusercontent.com/16686825/49084593-7c4ea800-f282-11e8-8b39-108bd9737f03.png)
  
## Movies
  ### Now playing by cities id 
  GET https://api.tix.id//v1/movies/now_playing?city_id=&tz=
  
  | Parameter  | Description  |
  |---|---|
  | city_id  | you can get city_id from Cities ID route  |
  | tz | 7  |
  ### Upcoming by cities id
  GET https://api.tix.id/v1/movies/upcoming?city_id=<city_id>
  
  | Parameter  | Description  |
  |---|---|
  | city_id  | you can get city_id from Cities ID route  |
 
## Theaters
   ### Get theaters in cities
   GET https://api.tix.id//v1/theaters?city_id=
   
  | Parameter  | Description  |
  |---|---|
  | city_id  | you can get city_id from Cities ID route  |
   
## Dana
  ### POST https://api.tix.id/v1/bind
  ```json
  {
	  "request_id": "143bf9ea-4949-4d78-becf-150e35a56d3e-1543314559895",
	  "user_id": "<your id>"
	}	
  ```
  
  ##### Response
  ![image](https://user-images.githubusercontent.com/16686825/49086031-13692f00-f286-11e8-898b-4c2be1905d49.png)
  
## Login TIXID
#### POST https://api.tix.id/v1/login/phone
```json
    {
      "msisdn": "<phone number>",
      "password": "<hashed password>"
    }
```
  note: idk know what hash type that TIXID used, you can reverse from APK that how hashed password work
  
  ##### Response
  
  ![login_resp](https://user-images.githubusercontent.com/16686825/49082744-23304580-f27d-11e8-9355-7a778a45b391.png)
  
  Save `X-Tix-Authorization` value from header response, this will be use later
  
  
  
 MORE API SOON
