## Authorization
There are 2 ways to send a subscription key in requests to API Management.

* Set the *Ocp-Apim-Subscription-Key* HTTP header - prefered and more secure
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
