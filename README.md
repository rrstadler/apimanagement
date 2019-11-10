# Azure API Management service

## Authorization
There are 2 ways to send a subscription key in requests to the Azure API Management proxy.

* Set the *Ocp-Apim-Subscription-Key* HTTP header - prefered and more secure (as not part of the URL query string)
* Set the *subscription-key* query string value in the URL - only use if HTTP header mechanism is not possible. e.g. As the query is part of the URL it is more likely to be logged .


e.g. 
Ocp-Apim-Subscription-Key: <your subscription key>


```
GET ****/services/River_Flood_WMS HTTP/1.1

Host: ****.azure-api.net
Cache-Control: no-cache
Ocp-Apim-Subscription-Key: ••••••••••••••••••••••••••••••••
```

or query parameter: subscription-key: <your subscription key>
```
GET ****/services/River_Flood_WMS?subscription-key=********* HTTP/1.1

Host: ****.azure-api.net
Cache-Control: no-cache
```

## How to get the subscription key
* You just subscribe to the API product in the API Management portal.
* It's possible to create new subscription key in a self service manner
