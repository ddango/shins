---
title: Vatware API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: false
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v3.6.6 -->

<section>
<h1 id="vatware-api">Vatware API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="https://uatvat-api.sovos.com">https://uatvat-api.sovos.com</a>

</section>

<section>
<h1 id="vatware-api-callback">Callback</h1>

<section>

## Handles a callback

<a id="opIdCallback_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://uatvat-api.sovos.com/api/callback \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://uatvat-api.sovos.com/api/callback HTTP/1.1
Host: uatvat-api.sovos.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "actionsOverride": [
    "string"
  ],
  "entities": [
    {
      "name": "string",
      "fields": [
        {
          "name": "string",
          "value": {}
        }
      ],
      "entities": [
        null
      ]
    }
  ],
  "messages": [
    {
      "description": "string",
      "legalStatusComments": "string",
      "legalTrackingId": "string",
      "processStartedTimestamp": "2019-05-23T21:00:10Z",
      "sendToErp": true
    }
  ],
  "attachments": [
    {
      "name": "string",
      "type": "string",
      "link": "string",
      "content": "string"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/callback',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://uatvat-api.sovos.com/api/callback',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://uatvat-api.sovos.com/api/callback', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://uatvat-api.sovos.com/api/callback', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/callback");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://uatvat-api.sovos.com/api/callback", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/callback`

> Body parameter

```json
{
  "actionsOverride": [
    "string"
  ],
  "entities": [
    {
      "name": "string",
      "fields": [
        {
          "name": "string",
          "value": {}
        }
      ],
      "entities": [
        null
      ]
    }
  ],
  "messages": [
    {
      "description": "string",
      "legalStatusComments": "string",
      "legalTrackingId": "string",
      "processStartedTimestamp": "2019-05-23T21:00:10Z",
      "sendToErp": true
    }
  ],
  "attachments": [
    {
      "name": "string",
      "type": "string",
      "link": "string",
      "content": "string"
    }
  ]
}
```

```yaml
actionsOverride:
  - string
entities:
  - name: string
    fields:
      - name: string
        value: {}
    entities:
      - null
messages:
  - description: string
    legalStatusComments: string
    legalTrackingId: string
    processStartedTimestamp: 2019-05-23T21:00:10Z
    sendToErp: true
attachments:
  - name: string
    type: string
    link: string
    content: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<TransmissionServiceRequest>
  <actionsOverride>string</actionsOverride>
  <entities>
    <name>string</name>
    <fields>
      <name>string</name>
      <value/>
    </fields>
    <entities/>
  </entities>
  <messages>
    <description>string</description>
    <legalStatusComments>string</legalStatusComments>
    <legalTrackingId>string</legalTrackingId>
    <processStartedTimestamp>2019-05-23T21:00:10Z</processStartedTimestamp>
    <sendToErp>true</sendToErp>
  </messages>
  <attachments>
    <name>string</name>
    <type>string</type>
    <link>string</link>
    <content>string</content>
  </attachments>
</TransmissionServiceRequest>
```

<section>
<h3 id="handles-a-callback-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[TransmissionServiceRequest](#schematransmissionservicerequest)|true|The specific company code to pull configuration for|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="handles-a-callback-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="handles-a-callback-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-configuration">Configuration</h1>

<section>

## Return the current configuration

<a id="opIdConfiguration_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://uatvat-api.sovos.com/api/configuration?companyCode=string&lastUpdated=2019-05-23T21%3A00%3A10Z \
  -H 'Accept: application/json'

```

```http
GET https://uatvat-api.sovos.com/api/configuration?companyCode=string&lastUpdated=2019-05-23T21%3A00%3A10Z HTTP/1.1
Host: uatvat-api.sovos.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/configuration?companyCode=string&lastUpdated=2019-05-23T21%3A00%3A10Z',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://uatvat-api.sovos.com/api/configuration',
  params: {
  'companyCode' => 'string',
'lastUpdated' => 'string(date-time)'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://uatvat-api.sovos.com/api/configuration', params={
  'companyCode': 'string',  'lastUpdated': '2019-05-23T21:00:10Z'
}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://uatvat-api.sovos.com/api/configuration', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/configuration?companyCode=string&lastUpdated=2019-05-23T21%3A00%3A10Z");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://uatvat-api.sovos.com/api/configuration", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/configuration`

<section>
<h3 id="return-the-current-configuration-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|companyCode|query|string|true|The specific company code to pull configuration for|
|lastUpdated|query|string(date-time)|true|The date the caller was last updated. Will return only changes since this date if specified.|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="return-the-current-configuration-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="return-the-current-configuration-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-inbound">Inbound</h1>

<section>

## Inbound_Index

<a id="opIdInbound_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://uatvat-api.sovos.com/api/inbound \
  -H 'Accept: application/json'

```

```http
POST https://uatvat-api.sovos.com/api/inbound HTTP/1.1
Host: uatvat-api.sovos.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/inbound',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.post 'https://uatvat-api.sovos.com/api/inbound',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('https://uatvat-api.sovos.com/api/inbound', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://uatvat-api.sovos.com/api/inbound', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/inbound");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://uatvat-api.sovos.com/api/inbound", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/inbound`

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="inbound_index-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="inbound_index-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-notifications">Notifications</h1>

<section>

## Notifications_Page

<a id="opIdNotifications_Page"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://uatvat-api.sovos.com/api/notifications?pageSize=0 \
  -H 'Accept: application/json'

```

```http
GET https://uatvat-api.sovos.com/api/notifications?pageSize=0 HTTP/1.1
Host: uatvat-api.sovos.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/notifications?pageSize=0',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://uatvat-api.sovos.com/api/notifications',
  params: {
  'pageSize' => 'integer(int32)'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://uatvat-api.sovos.com/api/notifications', params={
  'pageSize': '0'
}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://uatvat-api.sovos.com/api/notifications', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/notifications?pageSize=0");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://uatvat-api.sovos.com/api/notifications", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/notifications`

<section>
<h3 id="notifications_page-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|pageSize|query|integer(int32)|true|none|
|startIndex|query|integer(int32)|false|none|
|companyCode|query|string|false|none|

</section>

> Example responses

> 200 Response

```json
{
  "previous": "string",
  "next": "string",
  "totalPages": 0,
  "pageSize": 0,
  "startIndex": 0,
  "notifications": [
    {
      "notificationId": "string",
      "referenceId": "string",
      "companyCode": "string",
      "invoiceNumber": "string",
      "notificationCode": "string",
      "notificationDescription": "string",
      "notificationValue": "string",
      "notificationTimestamp": "2019-05-23T21:00:10Z",
      "acknowledgedNotification": true,
      "notificationProcessed": true,
      "companyName": "string",
      "notificationDateToDisplay": "string",
      "notificationOldValue": "string",
      "transactionField": "string",
      "notificationLink": "string",
      "erpDocument": "string",
      "environmentCode": "string"
    }
  ],
  "totalItems": 0
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ApiPageNotifications>
  <previous>string</previous>
  <next>string</next>
  <totalPages>0</totalPages>
  <pageSize>0</pageSize>
  <startIndex>0</startIndex>
  <notifications>
    <notificationId>string</notificationId>
    <referenceId>string</referenceId>
    <companyCode>string</companyCode>
    <invoiceNumber>string</invoiceNumber>
    <notificationCode>string</notificationCode>
    <notificationDescription>string</notificationDescription>
    <notificationValue>string</notificationValue>
    <notificationTimestamp>2019-05-23T21:00:10Z</notificationTimestamp>
    <acknowledgedNotification>true</acknowledgedNotification>
    <notificationProcessed>true</notificationProcessed>
    <companyName>string</companyName>
    <notificationDateToDisplay>string</notificationDateToDisplay>
    <notificationOldValue>string</notificationOldValue>
    <transactionField>string</transactionField>
    <notificationLink>string</notificationLink>
    <erpDocument>string</erpDocument>
    <environmentCode>string</environmentCode>
  </notifications>
  <totalItems>0</totalItems>
</ApiPageNotifications>
```

<section>
<h3 id="notifications_page-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ApiPageNotifications](#schemaapipagenotifications)|

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

<section>

## Marks the specified notification as read/acknowledged.

<a id="opIdNotifications_Acknowledge"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://uatvat-api.sovos.com/api/notifications \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT https://uatvat-api.sovos.com/api/notifications HTTP/1.1
Host: uatvat-api.sovos.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "notificationId": "string",
  "referenceId": "string",
  "companyCode": "string",
  "invoiceNumber": "string",
  "notificationCode": "string",
  "notificationDescription": "string",
  "notificationValue": "string",
  "notificationTimestamp": "2019-05-23T21:00:10Z",
  "acknowledgedNotification": true,
  "notificationProcessed": true,
  "companyName": "string",
  "notificationDateToDisplay": "string",
  "notificationOldValue": "string",
  "transactionField": "string",
  "notificationLink": "string",
  "erpDocument": "string",
  "environmentCode": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/notifications',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put 'https://uatvat-api.sovos.com/api/notifications',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('https://uatvat-api.sovos.com/api/notifications', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://uatvat-api.sovos.com/api/notifications', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/notifications");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://uatvat-api.sovos.com/api/notifications", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/notifications`

> Body parameter

```json
{
  "notificationId": "string",
  "referenceId": "string",
  "companyCode": "string",
  "invoiceNumber": "string",
  "notificationCode": "string",
  "notificationDescription": "string",
  "notificationValue": "string",
  "notificationTimestamp": "2019-05-23T21:00:10Z",
  "acknowledgedNotification": true,
  "notificationProcessed": true,
  "companyName": "string",
  "notificationDateToDisplay": "string",
  "notificationOldValue": "string",
  "transactionField": "string",
  "notificationLink": "string",
  "erpDocument": "string",
  "environmentCode": "string"
}
```

```yaml
notificationId: string
referenceId: string
companyCode: string
invoiceNumber: string
notificationCode: string
notificationDescription: string
notificationValue: string
notificationTimestamp: 2019-05-23T21:00:10Z
acknowledgedNotification: true
notificationProcessed: true
companyName: string
notificationDateToDisplay: string
notificationOldValue: string
transactionField: string
notificationLink: string
erpDocument: string
environmentCode: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ApiNotification>
  <notificationId>string</notificationId>
  <referenceId>string</referenceId>
  <companyCode>string</companyCode>
  <invoiceNumber>string</invoiceNumber>
  <notificationCode>string</notificationCode>
  <notificationDescription>string</notificationDescription>
  <notificationValue>string</notificationValue>
  <notificationTimestamp>2019-05-23T21:00:10Z</notificationTimestamp>
  <acknowledgedNotification>true</acknowledgedNotification>
  <notificationProcessed>true</notificationProcessed>
  <companyName>string</companyName>
  <notificationDateToDisplay>string</notificationDateToDisplay>
  <notificationOldValue>string</notificationOldValue>
  <transactionField>string</transactionField>
  <notificationLink>string</notificationLink>
  <erpDocument>string</erpDocument>
  <environmentCode>string</environmentCode>
</ApiNotification>
```

<section>
<h3 id="marks-the-specified-notification-as-read/acknowledged.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ApiNotification](#schemaapinotification)|true|notificationId must be specified|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="marks-the-specified-notification-as-read/acknowledged.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="marks-the-specified-notification-as-read/acknowledged.-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-notificationsv2">NotificationsV2</h1>

<section>

## Returns a list of notifications.

<a id="opIdNotificationsV2_Page"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://uatvat-api.sovos.com/api/v2/notifications \
  -H 'Accept: application/json'

```

```http
GET https://uatvat-api.sovos.com/api/v2/notifications HTTP/1.1
Host: uatvat-api.sovos.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/v2/notifications',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://uatvat-api.sovos.com/api/v2/notifications',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://uatvat-api.sovos.com/api/v2/notifications', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://uatvat-api.sovos.com/api/v2/notifications', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/v2/notifications");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://uatvat-api.sovos.com/api/v2/notifications", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/notifications`

<section>
<h3 id="returns-a-list-of-notifications.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|taxId|query|string|false|Tax ID of the company|
|docType|query|string|false|Document Type eg. OHUI|
|size|query|integer(int32)|false|default 50|
|processType|query|string|false|none|
|environmentCode|query|string|false|none|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="returns-a-list-of-notifications.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="returns-a-list-of-notifications.-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

<section>

## Marks the specified notification as read/acknowledged.

<a id="opIdNotificationsV2_Acknowledge"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://uatvat-api.sovos.com/api/v2/notifications \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT https://uatvat-api.sovos.com/api/v2/notifications HTTP/1.1
Host: uatvat-api.sovos.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "taxId": "string",
  "detail": [
    {
      "status": "string",
      "cloudId": "string"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/v2/notifications',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put 'https://uatvat-api.sovos.com/api/v2/notifications',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('https://uatvat-api.sovos.com/api/v2/notifications', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://uatvat-api.sovos.com/api/v2/notifications', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/v2/notifications");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://uatvat-api.sovos.com/api/v2/notifications", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/notifications`

> Body parameter

```json
{
  "taxId": "string",
  "detail": [
    {
      "status": "string",
      "cloudId": "string"
    }
  ]
}
```

```yaml
taxId: string
detail:
  - status: string
    cloudId: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ApiNotificationV2Ack>
  <taxId>string</taxId>
  <detail>
    <status>string</status>
    <cloudId>string</cloudId>
  </detail>
</ApiNotificationV2Ack>
```

<section>
<h3 id="marks-the-specified-notification-as-read/acknowledged.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ApiNotificationV2Ack](#schemaapinotificationv2ack)|true|none|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="marks-the-specified-notification-as-read/acknowledged.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="marks-the-specified-notification-as-read/acknowledged.-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-printerrule">PrinterRule</h1>

<section>

## Returns the report layout.

<a id="opIdPrinterRule_ExportReportLayout"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://uatvat-api.sovos.com/api/printerrule?id=0 \
  -H 'Accept: application/json'

```

```http
GET https://uatvat-api.sovos.com/api/printerrule?id=0 HTTP/1.1
Host: uatvat-api.sovos.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/printerrule?id=0',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://uatvat-api.sovos.com/api/printerrule',
  params: {
  'id' => 'integer(int32)'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://uatvat-api.sovos.com/api/printerrule', params={
  'id': '0'
}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://uatvat-api.sovos.com/api/printerrule', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/printerrule?id=0");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://uatvat-api.sovos.com/api/printerrule", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/printerrule`

<section>
<h3 id="returns-the-report-layout.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|integer(int32)|true|Printer Rule ID|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="returns-the-report-layout.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="returns-the-report-layout.-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-status">Status</h1>

<section>

## Returns simple up status. If the API is up, the string "VAT_API_IS_HEALTHY__ZZZZZ" will be returned.

<a id="opIdStatus_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://uatvat-api.sovos.com/api/status \
  -H 'Accept: application/json'

```

```http
GET https://uatvat-api.sovos.com/api/status HTTP/1.1
Host: uatvat-api.sovos.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/status',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://uatvat-api.sovos.com/api/status',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://uatvat-api.sovos.com/api/status', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://uatvat-api.sovos.com/api/status', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/status");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://uatvat-api.sovos.com/api/status", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/status`

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="returns-simple-up-status.-if-the-api-is-up,-the-string-"vat_api_is_healthy__zzzzz"-will-be-returned.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="returns-simple-up-status.-if-the-api-is-up,-the-string-"vat_api_is_healthy__zzzzz"-will-be-returned.-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-transactions">Transactions</h1>

<section>

## Transactions_Index

<a id="opIdTransactions_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://uatvat-api.sovos.com/api/transactions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
DELETE https://uatvat-api.sovos.com/api/transactions HTTP/1.1
Host: uatvat-api.sovos.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "companyCode": "string",
  "invoiceNumber": "string",
  "salesOrderNumber": "string",
  "purchaseOrderNumber": "string",
  "originalInvoiceNumber": "string",
  "currentApprovalStatus": "string",
  "documentType": "string",
  "sequencialNumberSalesBook": "string",
  "sequencialNumberPurchaseBook": "string",
  "transactionDate": "2019-05-23T21:00:10Z",
  "intrastatDate": "2019-05-23T21:00:10Z",
  "invoiceDate": "2019-05-23T21:00:10Z",
  "paymentDate": "2019-05-23T21:00:10Z",
  "reportDate": "2019-05-23T21:00:10Z",
  "invoiceType": "string",
  "invoiceCorrectionType": "string",
  "invoiceSelfBilled": true,
  "taxRegimeSales": "string",
  "taxRegimePurchases": "string",
  "customsNumber": "string",
  "customsDate": "2019-05-23T21:00:10Z",
  "paymentMethod": "string",
  "bankAccount": "string",
  "transactionCode": "string",
  "customsValue": "string",
  "erpDocument": "string",
  "referenceId": "string",
  "creditIndicator": "string",
  "lastInvoiceNumber": "string",
  "transactionIsDeleted": true,
  "accountingDocumentNumber": "string",
  "glDescription": "string",
  "glPostingDate": "2019-05-23T21:00:10Z",
  "fiscalYear": "string",
  "fiscalPeriod": "string",
  "erpFiscalPeriod": "string",
  "erpFiscalYear": "string",
  "establishmentCode": "string",
  "environmentCode": "string",
  "nFeNumber": "string",
  "nfNumber": "string",
  "nFeServiceNumber": "string",
  "nFeServiceIndicator": "string",
  "totalValue": 0,
  "totalValue2": 0,
  "seriesNumber": "string",
  "issuerID": "string",
  "partialDeduct": 0,
  "typeOfService": "string",
  "withholdingSubContractor": 0,
  "withholdingExemption": 0,
  "services15": 0,
  "services20": 0,
  "services25": 0,
  "additionalWithholdingExemption": 0,
  "cprbIndicator": "string",
  "customerIdType": "string",
  "creationDate": "2019-05-23T21:00:10Z",
  "creationTime": "string",
  "reversalOperation": 0,
  "reversalFiscalYear": 0,
  "reversalCompanyCode": "string",
  "reversalAccountingDocument": "string",
  "externalReference": "string",
  "originalLineNumberReference": "string",
  "registrationNumber": "string",
  "paymentConditions": "string",
  "supplierFiscalRepName": "string",
  "supplierFiscalRepAddress": "string",
  "supplierFiscalDescription": "string",
  "customerFiscalRepName": "string",
  "customerFiscalRepAddress": "string",
  "customerFiscalDescription": "string",
  "supplierCertifiedEmail": "string",
  "customerCertifiedEmail": "string",
  "supplierTIN": "string",
  "customerTIN": "string",
  "supplierEORICode": "string",
  "customerEORICode": "string",
  "supplierBIC": "string",
  "customer": {
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "supplier": {
    "invoiceNumber": "string",
    "invoiceLineNumber": "string",
    "originalInvoiceNumber": "string",
    "communicationType": "string",
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "lines": [
    {
      "currency": "string",
      "currency2": "string",
      "exchangeRate": 0,
      "vatCode": "string",
      "vatRate": "string",
      "itemDescription": "string",
      "itemClassification": "string",
      "taxableBasisCredit": 0,
      "taxableBasisDebet": 0,
      "valueVatCredit": 0,
      "valueVatDebet": 0,
      "totalValueLine": 0,
      "amountVatDeducted": 0,
      "taxableBasisCurrency2": 0,
      "valueVatCurrency2": 0,
      "totalValueLineCurrency2": 0,
      "countryDispatch": "string",
      "countryArrival": "string",
      "deliveryConditions": "string",
      "additionalDocumentReference": "string",
      "reportingType": "string",
      "transactionType": 0,
      "additionalTransactionType": 0,
      "intrastatCode": "string",
      "extrastatCode": "string",
      "additionalDescription": "string",
      "weight": 0,
      "unitOfMeasure": "string",
      "quantity": 0,
      "additionalUnitOfMeasure": "string",
      "commercialValue": 0,
      "statisticalValue": 0,
      "commercialValueCurrency2": 0,
      "statisticalValueCurrency2": 0,
      "itemType": "string",
      "modeOfTransport": 0,
      "regionDispatch": "string",
      "harbourDispatch": "string",
      "regionArrival": "string",
      "harbourArrival": "string",
      "countryOrigin": "string",
      "purchaseExtra1": "string",
      "purchaseExtra2": "string",
      "purchaseExtra3": "string",
      "purchaseExtra4": "string",
      "purchaseExtra5": "string",
      "purchaseExtra6": "string",
      "purchaseExtra7": "string",
      "purchaseExtra8": "string",
      "purchaseExtra9": "string",
      "purchaseExtra10": "string",
      "salesExtra1": "string",
      "salesExtra2": "string",
      "salesExtra3": "string",
      "salesExtra4": "string",
      "salesExtra5": "string",
      "salesExtra6": "string",
      "salesExtra7": "string",
      "salesExtra8": "string",
      "salesExtra9": "string",
      "salesExtra10": "string",
      "mossReporterVatNumberUsed": "string",
      "administrationCode": "string",
      "vatCodeAssignerCode": "string",
      "isOriginal": true,
      "deliveryConditionsPlace": "string",
      "regionOrigin": "string",
      "vatCodeAccountingKey": "string",
      "originalTaxRateApplied": "string",
      "originalVatcodeUsed": "string",
      "originalVatcodeUsedDescription": "string",
      "vatGlAccountCredit": "string",
      "vatGlAccountDebet": "string",
      "vatGlAccountPurchases": "string",
      "vatGlAccountSales": "string",
      "revenuesGlAccount": "string",
      "costsGlAccount": "string",
      "plantCode": "string",
      "materialTaxClassification": "string",
      "customerTaxClassification": "string",
      "invoiceLineNumber": "string",
      "unitPrice": 0,
      "creditNoteReason": "string",
      "generalLedgerId": "string",
      "generalLedgerType": "string",
      "journalDescription": "string",
      "journalId": "string",
      "journalType": "string",
      "statisticalProcedure": "string",
      "propertyCode": "string",
      "propertyRegisterReference": "string",
      "exemptReasonCode": "string",
      "utilizationDate": "2019-05-23T21:00:10Z",
      "annualProrate": 0,
      "annualDeduction": 0,
      "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
      "assetId": "string",
      "deliveryIdentification": "string",
      "firstSemester": true,
      "withholdingAmount": 0,
      "operationType": "string",
      "profitCenter": "string",
      "discountBaseAmount": 0,
      "businessArea": "string",
      "costCenter": "string",
      "materialNumber": "string",
      "assignmentNumber": "string",
      "projectNumber": "string",
      "establishmentCode": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "exchangeRate2": 0,
      "withholdingType": "string",
      "withholdingRate": 0,
      "withholdingDescription": "string",
      "salesOrderDate": "2019-05-23T21:00:10Z",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "shipperCountryVATNumber": "string",
      "shipperCountryVATNumberUsed": "string",
      "shipperName": "string",
      "shipperLocalCode": "string",
      "shipmentType": "string",
      "shipmentDescription": "string",
      "shipmentWeightUOM": "string",
      "shipmentWeightGross": 0,
      "shipmentWeightNet": 0,
      "shipmentDateTime": "2019-05-23T21:00:10Z",
      "itemCodeType": "string",
      "itemCode": "string",
      "transactionEndDate": "2019-05-23T21:00:10Z",
      "paymentExpireDate": "2019-05-23T21:00:10Z",
      "paymentBankName": "string",
      "paymentCode": "string",
      "intBankAccountNumber": "string",
      "originalInvoiceDate": "2019-05-23T21:00:10Z",
      "shipmentNumofPackages": 0,
      "paymentDueDate": 0,
      "vatDueDate": "string",
      "virtualStamp": "string",
      "stampAmount": 0,
      "reaOffice": "string",
      "reaNumber": "string",
      "socialCapital": 0,
      "soleShareholder": "string",
      "statusLiquidation": "string",
      "referenceProvision": "string",
      "doacupCode": "string",
      "doacigCode": "string",
      "dtCtrDocumentID": "string",
      "dtCtrDate": "2019-05-23T21:00:10Z",
      "dtCtrItemNum": "string",
      "dtCtrConvCode": "string",
      "dtCtrCUPCode": "string",
      "dtCtrCIGCode": "string",
      "dtCnvDocumentID": "string",
      "dtCnvDate": "2019-05-23T21:00:10Z",
      "dtCnvItemNum": "string",
      "dtCnvConvCode": "string",
      "dtCnvCUPCode": "string",
      "dtCnvCIGCode": "string",
      "dtRczDocumentID": "string",
      "dtRczDate": "2019-05-23T21:00:10Z",
      "dtRczItemNum": "string",
      "dtRczConvCode": "string",
      "dtRczCUPCode": "string",
      "dtRczCIGCode": "string",
      "adGestionaliType": "string",
      "adGestionaliText": "string",
      "adGestionaliNumber": 0,
      "adGestionaliDate": "2019-05-23T21:00:10Z",
      "adGestionaliType2": "string",
      "adGestionaliText2": "string",
      "adGestionaliType3": "string",
      "adGestionaliText3": "string",
      "adGestionaliType4": "string",
      "adGestionaliText4": "string",
      "adGestionaliType5": "string",
      "adGestionaliText5": "string",
      "lineNature": "string",
      "lineAdminReference": "string",
      "shipmentCause": "string",
      "shipTimeStamp": "2019-05-23T21:00:10Z",
      "shipmentStartDate": "2019-05-23T21:00:10Z",
      "alboProfessional": "string",
      "alboProvince": "string",
      "alboInscriptionDate": "2019-05-23T21:00:10Z",
      "supplierLocalOfficeAddress": "string",
      "supplierLocalOfficeStreetNumber": "string",
      "supplierLocalOfficePostalCode": 0,
      "supplierLocalOfficeCity": "string",
      "supplierLocalOfficeProvince": "string",
      "supplierLocalOfficeCountry": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepTIN": "string",
      "supplierFiscalRepFirstName": "string",
      "supplierFiscalRepLastName": "string",
      "supplierFiscalRepCodEORI": "string",
      "customerLocalOfficeAddress": "string",
      "customerLocalOfficeStreetNumber": "string",
      "customerLocalOfficePostalCode": 0,
      "customerLocalOfficeCity": "string",
      "customerLocalOfficeProvince": "string",
      "customerLocalOfficeCountry": "string",
      "customerFiscalRepFirstName": "string",
      "customerFiscalRepLastName": "string",
      "roundingAmount": 0,
      "socSecType": "string",
      "socSecRate": 0,
      "socSecContributionAmount": 0,
      "socSecTaxableAmount": 0,
      "socSecVATRate": 0,
      "socSecWithheld": "string",
      "socSecNatura": "string",
      "socSecAdminReference": "string",
      "art73": "string",
      "stageReference": 0,
      "shipperTIN": "string",
      "driverFirstName": "string",
      "driverLastName": "string",
      "resaType": "string",
      "mainInvoiceNumber": "string",
      "mainInvoiceDate": "2019-05-23T21:00:10Z",
      "subjectWithheld": "string",
      "additionalExpenses": 0,
      "paymentRoundingAmount": 0,
      "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
      "vehicleTotalTravel": "string",
      "paymentBeneficiary": "string",
      "officePostalCode": "string",
      "signerLastName": "string",
      "signerFirstName": "string",
      "signerTIN": "string",
      "abiCode": 0,
      "cabCode": 0,
      "prepaymentDiscount": 0,
      "prepaymentDueDate": "2019-05-23T21:00:10Z",
      "penaltyLatePayment": 0,
      "penaltyStartDate": "2019-05-23T21:00:10Z",
      "supplierFiscalRepTitle": "string",
      "driverTitle": "string",
      "doaNumItem": "string",
      "supplierFiscalRepCountryVATNumber": "string",
      "customerFiscalRepCountryVATNumber": "string",
      "salesOrderNumber2": "string",
      "salesOrderNumber3": "string",
      "salesOrderNumber4": "string",
      "salesOrderNumber5": "string"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/transactions',
{
  method: 'DELETE',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.delete 'https://uatvat-api.sovos.com/api/transactions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.delete('https://uatvat-api.sovos.com/api/transactions', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://uatvat-api.sovos.com/api/transactions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/transactions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://uatvat-api.sovos.com/api/transactions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/transactions`

> Body parameter

```json
{
  "companyCode": "string",
  "invoiceNumber": "string",
  "salesOrderNumber": "string",
  "purchaseOrderNumber": "string",
  "originalInvoiceNumber": "string",
  "currentApprovalStatus": "string",
  "documentType": "string",
  "sequencialNumberSalesBook": "string",
  "sequencialNumberPurchaseBook": "string",
  "transactionDate": "2019-05-23T21:00:10Z",
  "intrastatDate": "2019-05-23T21:00:10Z",
  "invoiceDate": "2019-05-23T21:00:10Z",
  "paymentDate": "2019-05-23T21:00:10Z",
  "reportDate": "2019-05-23T21:00:10Z",
  "invoiceType": "string",
  "invoiceCorrectionType": "string",
  "invoiceSelfBilled": true,
  "taxRegimeSales": "string",
  "taxRegimePurchases": "string",
  "customsNumber": "string",
  "customsDate": "2019-05-23T21:00:10Z",
  "paymentMethod": "string",
  "bankAccount": "string",
  "transactionCode": "string",
  "customsValue": "string",
  "erpDocument": "string",
  "referenceId": "string",
  "creditIndicator": "string",
  "lastInvoiceNumber": "string",
  "transactionIsDeleted": true,
  "accountingDocumentNumber": "string",
  "glDescription": "string",
  "glPostingDate": "2019-05-23T21:00:10Z",
  "fiscalYear": "string",
  "fiscalPeriod": "string",
  "erpFiscalPeriod": "string",
  "erpFiscalYear": "string",
  "establishmentCode": "string",
  "environmentCode": "string",
  "nFeNumber": "string",
  "nfNumber": "string",
  "nFeServiceNumber": "string",
  "nFeServiceIndicator": "string",
  "totalValue": 0,
  "totalValue2": 0,
  "seriesNumber": "string",
  "issuerID": "string",
  "partialDeduct": 0,
  "typeOfService": "string",
  "withholdingSubContractor": 0,
  "withholdingExemption": 0,
  "services15": 0,
  "services20": 0,
  "services25": 0,
  "additionalWithholdingExemption": 0,
  "cprbIndicator": "string",
  "customerIdType": "string",
  "creationDate": "2019-05-23T21:00:10Z",
  "creationTime": "string",
  "reversalOperation": 0,
  "reversalFiscalYear": 0,
  "reversalCompanyCode": "string",
  "reversalAccountingDocument": "string",
  "externalReference": "string",
  "originalLineNumberReference": "string",
  "registrationNumber": "string",
  "paymentConditions": "string",
  "supplierFiscalRepName": "string",
  "supplierFiscalRepAddress": "string",
  "supplierFiscalDescription": "string",
  "customerFiscalRepName": "string",
  "customerFiscalRepAddress": "string",
  "customerFiscalDescription": "string",
  "supplierCertifiedEmail": "string",
  "customerCertifiedEmail": "string",
  "supplierTIN": "string",
  "customerTIN": "string",
  "supplierEORICode": "string",
  "customerEORICode": "string",
  "supplierBIC": "string",
  "customer": {
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "supplier": {
    "invoiceNumber": "string",
    "invoiceLineNumber": "string",
    "originalInvoiceNumber": "string",
    "communicationType": "string",
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "lines": [
    {
      "currency": "string",
      "currency2": "string",
      "exchangeRate": 0,
      "vatCode": "string",
      "vatRate": "string",
      "itemDescription": "string",
      "itemClassification": "string",
      "taxableBasisCredit": 0,
      "taxableBasisDebet": 0,
      "valueVatCredit": 0,
      "valueVatDebet": 0,
      "totalValueLine": 0,
      "amountVatDeducted": 0,
      "taxableBasisCurrency2": 0,
      "valueVatCurrency2": 0,
      "totalValueLineCurrency2": 0,
      "countryDispatch": "string",
      "countryArrival": "string",
      "deliveryConditions": "string",
      "additionalDocumentReference": "string",
      "reportingType": "string",
      "transactionType": 0,
      "additionalTransactionType": 0,
      "intrastatCode": "string",
      "extrastatCode": "string",
      "additionalDescription": "string",
      "weight": 0,
      "unitOfMeasure": "string",
      "quantity": 0,
      "additionalUnitOfMeasure": "string",
      "commercialValue": 0,
      "statisticalValue": 0,
      "commercialValueCurrency2": 0,
      "statisticalValueCurrency2": 0,
      "itemType": "string",
      "modeOfTransport": 0,
      "regionDispatch": "string",
      "harbourDispatch": "string",
      "regionArrival": "string",
      "harbourArrival": "string",
      "countryOrigin": "string",
      "purchaseExtra1": "string",
      "purchaseExtra2": "string",
      "purchaseExtra3": "string",
      "purchaseExtra4": "string",
      "purchaseExtra5": "string",
      "purchaseExtra6": "string",
      "purchaseExtra7": "string",
      "purchaseExtra8": "string",
      "purchaseExtra9": "string",
      "purchaseExtra10": "string",
      "salesExtra1": "string",
      "salesExtra2": "string",
      "salesExtra3": "string",
      "salesExtra4": "string",
      "salesExtra5": "string",
      "salesExtra6": "string",
      "salesExtra7": "string",
      "salesExtra8": "string",
      "salesExtra9": "string",
      "salesExtra10": "string",
      "mossReporterVatNumberUsed": "string",
      "administrationCode": "string",
      "vatCodeAssignerCode": "string",
      "isOriginal": true,
      "deliveryConditionsPlace": "string",
      "regionOrigin": "string",
      "vatCodeAccountingKey": "string",
      "originalTaxRateApplied": "string",
      "originalVatcodeUsed": "string",
      "originalVatcodeUsedDescription": "string",
      "vatGlAccountCredit": "string",
      "vatGlAccountDebet": "string",
      "vatGlAccountPurchases": "string",
      "vatGlAccountSales": "string",
      "revenuesGlAccount": "string",
      "costsGlAccount": "string",
      "plantCode": "string",
      "materialTaxClassification": "string",
      "customerTaxClassification": "string",
      "invoiceLineNumber": "string",
      "unitPrice": 0,
      "creditNoteReason": "string",
      "generalLedgerId": "string",
      "generalLedgerType": "string",
      "journalDescription": "string",
      "journalId": "string",
      "journalType": "string",
      "statisticalProcedure": "string",
      "propertyCode": "string",
      "propertyRegisterReference": "string",
      "exemptReasonCode": "string",
      "utilizationDate": "2019-05-23T21:00:10Z",
      "annualProrate": 0,
      "annualDeduction": 0,
      "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
      "assetId": "string",
      "deliveryIdentification": "string",
      "firstSemester": true,
      "withholdingAmount": 0,
      "operationType": "string",
      "profitCenter": "string",
      "discountBaseAmount": 0,
      "businessArea": "string",
      "costCenter": "string",
      "materialNumber": "string",
      "assignmentNumber": "string",
      "projectNumber": "string",
      "establishmentCode": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "exchangeRate2": 0,
      "withholdingType": "string",
      "withholdingRate": 0,
      "withholdingDescription": "string",
      "salesOrderDate": "2019-05-23T21:00:10Z",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "shipperCountryVATNumber": "string",
      "shipperCountryVATNumberUsed": "string",
      "shipperName": "string",
      "shipperLocalCode": "string",
      "shipmentType": "string",
      "shipmentDescription": "string",
      "shipmentWeightUOM": "string",
      "shipmentWeightGross": 0,
      "shipmentWeightNet": 0,
      "shipmentDateTime": "2019-05-23T21:00:10Z",
      "itemCodeType": "string",
      "itemCode": "string",
      "transactionEndDate": "2019-05-23T21:00:10Z",
      "paymentExpireDate": "2019-05-23T21:00:10Z",
      "paymentBankName": "string",
      "paymentCode": "string",
      "intBankAccountNumber": "string",
      "originalInvoiceDate": "2019-05-23T21:00:10Z",
      "shipmentNumofPackages": 0,
      "paymentDueDate": 0,
      "vatDueDate": "string",
      "virtualStamp": "string",
      "stampAmount": 0,
      "reaOffice": "string",
      "reaNumber": "string",
      "socialCapital": 0,
      "soleShareholder": "string",
      "statusLiquidation": "string",
      "referenceProvision": "string",
      "doacupCode": "string",
      "doacigCode": "string",
      "dtCtrDocumentID": "string",
      "dtCtrDate": "2019-05-23T21:00:10Z",
      "dtCtrItemNum": "string",
      "dtCtrConvCode": "string",
      "dtCtrCUPCode": "string",
      "dtCtrCIGCode": "string",
      "dtCnvDocumentID": "string",
      "dtCnvDate": "2019-05-23T21:00:10Z",
      "dtCnvItemNum": "string",
      "dtCnvConvCode": "string",
      "dtCnvCUPCode": "string",
      "dtCnvCIGCode": "string",
      "dtRczDocumentID": "string",
      "dtRczDate": "2019-05-23T21:00:10Z",
      "dtRczItemNum": "string",
      "dtRczConvCode": "string",
      "dtRczCUPCode": "string",
      "dtRczCIGCode": "string",
      "adGestionaliType": "string",
      "adGestionaliText": "string",
      "adGestionaliNumber": 0,
      "adGestionaliDate": "2019-05-23T21:00:10Z",
      "adGestionaliType2": "string",
      "adGestionaliText2": "string",
      "adGestionaliType3": "string",
      "adGestionaliText3": "string",
      "adGestionaliType4": "string",
      "adGestionaliText4": "string",
      "adGestionaliType5": "string",
      "adGestionaliText5": "string",
      "lineNature": "string",
      "lineAdminReference": "string",
      "shipmentCause": "string",
      "shipTimeStamp": "2019-05-23T21:00:10Z",
      "shipmentStartDate": "2019-05-23T21:00:10Z",
      "alboProfessional": "string",
      "alboProvince": "string",
      "alboInscriptionDate": "2019-05-23T21:00:10Z",
      "supplierLocalOfficeAddress": "string",
      "supplierLocalOfficeStreetNumber": "string",
      "supplierLocalOfficePostalCode": 0,
      "supplierLocalOfficeCity": "string",
      "supplierLocalOfficeProvince": "string",
      "supplierLocalOfficeCountry": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepTIN": "string",
      "supplierFiscalRepFirstName": "string",
      "supplierFiscalRepLastName": "string",
      "supplierFiscalRepCodEORI": "string",
      "customerLocalOfficeAddress": "string",
      "customerLocalOfficeStreetNumber": "string",
      "customerLocalOfficePostalCode": 0,
      "customerLocalOfficeCity": "string",
      "customerLocalOfficeProvince": "string",
      "customerLocalOfficeCountry": "string",
      "customerFiscalRepFirstName": "string",
      "customerFiscalRepLastName": "string",
      "roundingAmount": 0,
      "socSecType": "string",
      "socSecRate": 0,
      "socSecContributionAmount": 0,
      "socSecTaxableAmount": 0,
      "socSecVATRate": 0,
      "socSecWithheld": "string",
      "socSecNatura": "string",
      "socSecAdminReference": "string",
      "art73": "string",
      "stageReference": 0,
      "shipperTIN": "string",
      "driverFirstName": "string",
      "driverLastName": "string",
      "resaType": "string",
      "mainInvoiceNumber": "string",
      "mainInvoiceDate": "2019-05-23T21:00:10Z",
      "subjectWithheld": "string",
      "additionalExpenses": 0,
      "paymentRoundingAmount": 0,
      "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
      "vehicleTotalTravel": "string",
      "paymentBeneficiary": "string",
      "officePostalCode": "string",
      "signerLastName": "string",
      "signerFirstName": "string",
      "signerTIN": "string",
      "abiCode": 0,
      "cabCode": 0,
      "prepaymentDiscount": 0,
      "prepaymentDueDate": "2019-05-23T21:00:10Z",
      "penaltyLatePayment": 0,
      "penaltyStartDate": "2019-05-23T21:00:10Z",
      "supplierFiscalRepTitle": "string",
      "driverTitle": "string",
      "doaNumItem": "string",
      "supplierFiscalRepCountryVATNumber": "string",
      "customerFiscalRepCountryVATNumber": "string",
      "salesOrderNumber2": "string",
      "salesOrderNumber3": "string",
      "salesOrderNumber4": "string",
      "salesOrderNumber5": "string"
    }
  ]
}
```

```yaml
companyCode: string
invoiceNumber: string
salesOrderNumber: string
purchaseOrderNumber: string
originalInvoiceNumber: string
currentApprovalStatus: string
documentType: string
sequencialNumberSalesBook: string
sequencialNumberPurchaseBook: string
transactionDate: 2019-05-23T21:00:10Z
intrastatDate: 2019-05-23T21:00:10Z
invoiceDate: 2019-05-23T21:00:10Z
paymentDate: 2019-05-23T21:00:10Z
reportDate: 2019-05-23T21:00:10Z
invoiceType: string
invoiceCorrectionType: string
invoiceSelfBilled: true
taxRegimeSales: string
taxRegimePurchases: string
customsNumber: string
customsDate: 2019-05-23T21:00:10Z
paymentMethod: string
bankAccount: string
transactionCode: string
customsValue: string
erpDocument: string
referenceId: string
creditIndicator: string
lastInvoiceNumber: string
transactionIsDeleted: true
accountingDocumentNumber: string
glDescription: string
glPostingDate: 2019-05-23T21:00:10Z
fiscalYear: string
fiscalPeriod: string
erpFiscalPeriod: string
erpFiscalYear: string
establishmentCode: string
environmentCode: string
nFeNumber: string
nfNumber: string
nFeServiceNumber: string
nFeServiceIndicator: string
totalValue: 0
totalValue2: 0
seriesNumber: string
issuerID: string
partialDeduct: 0
typeOfService: string
withholdingSubContractor: 0
withholdingExemption: 0
services15: 0
services20: 0
services25: 0
additionalWithholdingExemption: 0
cprbIndicator: string
customerIdType: string
creationDate: 2019-05-23T21:00:10Z
creationTime: string
reversalOperation: 0
reversalFiscalYear: 0
reversalCompanyCode: string
reversalAccountingDocument: string
externalReference: string
originalLineNumberReference: string
registrationNumber: string
paymentConditions: string
supplierFiscalRepName: string
supplierFiscalRepAddress: string
supplierFiscalDescription: string
customerFiscalRepName: string
customerFiscalRepAddress: string
customerFiscalDescription: string
supplierCertifiedEmail: string
customerCertifiedEmail: string
supplierTIN: string
customerTIN: string
supplierEORICode: string
customerEORICode: string
supplierBIC: string
customer:
  businessEntityID: string
  name: string
  billToCountry: string
  vatNumberUsed: string
  countryVatNumberUsed: string
  billToStreet: string
  billToBuildingNumber: string
  billToCity: string
  billToPostalCode: string
  ucr: string
  website: string
  billToAddressDetail: string
  billToRegion: string
  billToStreetNumber: string
  contactFirstName: string
  contactLastName: string
  contactTitle: string
  contactVATNumber: string
  deliveryDate: 2019-05-23T21:00:10Z
  deliveryId: string
  emailAddress: string
  faxNumber: string
  shipFromAddressDetail: string
  shipFromBuildingNumber: string
  shipFromCity: string
  shipFromCountry: string
  shipFromLocationId: string
  shipFromPostalCode: string
  shipFromRegion: string
  shipFromStreet: string
  shipFromStreetNumber: string
  shipFromWarehouseId: string
  shipToAddressDetail: string
  shipToBuildingNumber: string
  shipToCity: string
  shipToCountry: string
  shipToLocationId: string
  shipToPostalCode: string
  shipToRegion: string
  shipToStreet: string
  shipToStreetNumber: string
  shipToWarehouseId: string
  telephoneNumber: string
  fiscalRepVATNumber: string
  idType: string
  idNumber: string
  localTaxNumber: string
supplier:
  invoiceNumber: string
  invoiceLineNumber: string
  originalInvoiceNumber: string
  communicationType: string
  businessEntityID: string
  name: string
  billToCountry: string
  vatNumberUsed: string
  countryVatNumberUsed: string
  billToStreet: string
  billToBuildingNumber: string
  billToCity: string
  billToPostalCode: string
  ucr: string
  website: string
  billToAddressDetail: string
  billToRegion: string
  billToStreetNumber: string
  contactFirstName: string
  contactLastName: string
  contactTitle: string
  contactVATNumber: string
  deliveryDate: 2019-05-23T21:00:10Z
  deliveryId: string
  emailAddress: string
  faxNumber: string
  shipFromAddressDetail: string
  shipFromBuildingNumber: string
  shipFromCity: string
  shipFromCountry: string
  shipFromLocationId: string
  shipFromPostalCode: string
  shipFromRegion: string
  shipFromStreet: string
  shipFromStreetNumber: string
  shipFromWarehouseId: string
  shipToAddressDetail: string
  shipToBuildingNumber: string
  shipToCity: string
  shipToCountry: string
  shipToLocationId: string
  shipToPostalCode: string
  shipToRegion: string
  shipToStreet: string
  shipToStreetNumber: string
  shipToWarehouseId: string
  telephoneNumber: string
  fiscalRepVATNumber: string
  idType: string
  idNumber: string
  localTaxNumber: string
lines:
  - currency: string
    currency2: string
    exchangeRate: 0
    vatCode: string
    vatRate: string
    itemDescription: string
    itemClassification: string
    taxableBasisCredit: 0
    taxableBasisDebet: 0
    valueVatCredit: 0
    valueVatDebet: 0
    totalValueLine: 0
    amountVatDeducted: 0
    taxableBasisCurrency2: 0
    valueVatCurrency2: 0
    totalValueLineCurrency2: 0
    countryDispatch: string
    countryArrival: string
    deliveryConditions: string
    additionalDocumentReference: string
    reportingType: string
    transactionType: 0
    additionalTransactionType: 0
    intrastatCode: string
    extrastatCode: string
    additionalDescription: string
    weight: 0
    unitOfMeasure: string
    quantity: 0
    additionalUnitOfMeasure: string
    commercialValue: 0
    statisticalValue: 0
    commercialValueCurrency2: 0
    statisticalValueCurrency2: 0
    itemType: string
    modeOfTransport: 0
    regionDispatch: string
    harbourDispatch: string
    regionArrival: string
    harbourArrival: string
    countryOrigin: string
    purchaseExtra1: string
    purchaseExtra2: string
    purchaseExtra3: string
    purchaseExtra4: string
    purchaseExtra5: string
    purchaseExtra6: string
    purchaseExtra7: string
    purchaseExtra8: string
    purchaseExtra9: string
    purchaseExtra10: string
    salesExtra1: string
    salesExtra2: string
    salesExtra3: string
    salesExtra4: string
    salesExtra5: string
    salesExtra6: string
    salesExtra7: string
    salesExtra8: string
    salesExtra9: string
    salesExtra10: string
    mossReporterVatNumberUsed: string
    administrationCode: string
    vatCodeAssignerCode: string
    isOriginal: true
    deliveryConditionsPlace: string
    regionOrigin: string
    vatCodeAccountingKey: string
    originalTaxRateApplied: string
    originalVatcodeUsed: string
    originalVatcodeUsedDescription: string
    vatGlAccountCredit: string
    vatGlAccountDebet: string
    vatGlAccountPurchases: string
    vatGlAccountSales: string
    revenuesGlAccount: string
    costsGlAccount: string
    plantCode: string
    materialTaxClassification: string
    customerTaxClassification: string
    invoiceLineNumber: string
    unitPrice: 0
    creditNoteReason: string
    generalLedgerId: string
    generalLedgerType: string
    journalDescription: string
    journalId: string
    journalType: string
    statisticalProcedure: string
    propertyCode: string
    propertyRegisterReference: string
    exemptReasonCode: string
    utilizationDate: 2019-05-23T21:00:10Z
    annualProrate: 0
    annualDeduction: 0
    annualDeductionEffectiveDate: 2019-05-23T21:00:10Z
    assetId: string
    deliveryIdentification: string
    firstSemester: true
    withholdingAmount: 0
    operationType: string
    profitCenter: string
    discountBaseAmount: 0
    businessArea: string
    costCenter: string
    materialNumber: string
    assignmentNumber: string
    projectNumber: string
    establishmentCode: string
    creationDate: 2019-05-23T21:00:10Z
    creationTime: string
    exchangeRate2: 0
    withholdingType: string
    withholdingRate: 0
    withholdingDescription: string
    salesOrderDate: 2019-05-23T21:00:10Z
    salesOrderNumber: string
    purchaseOrderNumber: string
    shipperCountryVATNumber: string
    shipperCountryVATNumberUsed: string
    shipperName: string
    shipperLocalCode: string
    shipmentType: string
    shipmentDescription: string
    shipmentWeightUOM: string
    shipmentWeightGross: 0
    shipmentWeightNet: 0
    shipmentDateTime: 2019-05-23T21:00:10Z
    itemCodeType: string
    itemCode: string
    transactionEndDate: 2019-05-23T21:00:10Z
    paymentExpireDate: 2019-05-23T21:00:10Z
    paymentBankName: string
    paymentCode: string
    intBankAccountNumber: string
    originalInvoiceDate: 2019-05-23T21:00:10Z
    shipmentNumofPackages: 0
    paymentDueDate: 0
    vatDueDate: string
    virtualStamp: string
    stampAmount: 0
    reaOffice: string
    reaNumber: string
    socialCapital: 0
    soleShareholder: string
    statusLiquidation: string
    referenceProvision: string
    doacupCode: string
    doacigCode: string
    dtCtrDocumentID: string
    dtCtrDate: 2019-05-23T21:00:10Z
    dtCtrItemNum: string
    dtCtrConvCode: string
    dtCtrCUPCode: string
    dtCtrCIGCode: string
    dtCnvDocumentID: string
    dtCnvDate: 2019-05-23T21:00:10Z
    dtCnvItemNum: string
    dtCnvConvCode: string
    dtCnvCUPCode: string
    dtCnvCIGCode: string
    dtRczDocumentID: string
    dtRczDate: 2019-05-23T21:00:10Z
    dtRczItemNum: string
    dtRczConvCode: string
    dtRczCUPCode: string
    dtRczCIGCode: string
    adGestionaliType: string
    adGestionaliText: string
    adGestionaliNumber: 0
    adGestionaliDate: 2019-05-23T21:00:10Z
    adGestionaliType2: string
    adGestionaliText2: string
    adGestionaliType3: string
    adGestionaliText3: string
    adGestionaliType4: string
    adGestionaliText4: string
    adGestionaliType5: string
    adGestionaliText5: string
    lineNature: string
    lineAdminReference: string
    shipmentCause: string
    shipTimeStamp: 2019-05-23T21:00:10Z
    shipmentStartDate: 2019-05-23T21:00:10Z
    alboProfessional: string
    alboProvince: string
    alboInscriptionDate: 2019-05-23T21:00:10Z
    supplierLocalOfficeAddress: string
    supplierLocalOfficeStreetNumber: string
    supplierLocalOfficePostalCode: 0
    supplierLocalOfficeCity: string
    supplierLocalOfficeProvince: string
    supplierLocalOfficeCountry: string
    supplierFiscalRepName: string
    supplierFiscalRepTIN: string
    supplierFiscalRepFirstName: string
    supplierFiscalRepLastName: string
    supplierFiscalRepCodEORI: string
    customerLocalOfficeAddress: string
    customerLocalOfficeStreetNumber: string
    customerLocalOfficePostalCode: 0
    customerLocalOfficeCity: string
    customerLocalOfficeProvince: string
    customerLocalOfficeCountry: string
    customerFiscalRepFirstName: string
    customerFiscalRepLastName: string
    roundingAmount: 0
    socSecType: string
    socSecRate: 0
    socSecContributionAmount: 0
    socSecTaxableAmount: 0
    socSecVATRate: 0
    socSecWithheld: string
    socSecNatura: string
    socSecAdminReference: string
    art73: string
    stageReference: 0
    shipperTIN: string
    driverFirstName: string
    driverLastName: string
    resaType: string
    mainInvoiceNumber: string
    mainInvoiceDate: 2019-05-23T21:00:10Z
    subjectWithheld: string
    additionalExpenses: 0
    paymentRoundingAmount: 0
    vehicleRegistrationDate: 2019-05-23T21:00:10Z
    vehicleTotalTravel: string
    paymentBeneficiary: string
    officePostalCode: string
    signerLastName: string
    signerFirstName: string
    signerTIN: string
    abiCode: 0
    cabCode: 0
    prepaymentDiscount: 0
    prepaymentDueDate: 2019-05-23T21:00:10Z
    penaltyLatePayment: 0
    penaltyStartDate: 2019-05-23T21:00:10Z
    supplierFiscalRepTitle: string
    driverTitle: string
    doaNumItem: string
    supplierFiscalRepCountryVATNumber: string
    customerFiscalRepCountryVATNumber: string
    salesOrderNumber2: string
    salesOrderNumber3: string
    salesOrderNumber4: string
    salesOrderNumber5: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ApiTransaction>
  <companyCode>string</companyCode>
  <invoiceNumber>string</invoiceNumber>
  <salesOrderNumber>string</salesOrderNumber>
  <purchaseOrderNumber>string</purchaseOrderNumber>
  <originalInvoiceNumber>string</originalInvoiceNumber>
  <currentApprovalStatus>string</currentApprovalStatus>
  <documentType>string</documentType>
  <sequencialNumberSalesBook>string</sequencialNumberSalesBook>
  <sequencialNumberPurchaseBook>string</sequencialNumberPurchaseBook>
  <transactionDate>2019-05-23T21:00:10Z</transactionDate>
  <intrastatDate>2019-05-23T21:00:10Z</intrastatDate>
  <invoiceDate>2019-05-23T21:00:10Z</invoiceDate>
  <paymentDate>2019-05-23T21:00:10Z</paymentDate>
  <reportDate>2019-05-23T21:00:10Z</reportDate>
  <invoiceType>string</invoiceType>
  <invoiceCorrectionType>string</invoiceCorrectionType>
  <invoiceSelfBilled>true</invoiceSelfBilled>
  <taxRegimeSales>string</taxRegimeSales>
  <taxRegimePurchases>string</taxRegimePurchases>
  <customsNumber>string</customsNumber>
  <customsDate>2019-05-23T21:00:10Z</customsDate>
  <paymentMethod>string</paymentMethod>
  <bankAccount>string</bankAccount>
  <transactionCode>string</transactionCode>
  <customsValue>string</customsValue>
  <erpDocument>string</erpDocument>
  <referenceId>string</referenceId>
  <creditIndicator>string</creditIndicator>
  <lastInvoiceNumber>string</lastInvoiceNumber>
  <transactionIsDeleted>true</transactionIsDeleted>
  <accountingDocumentNumber>string</accountingDocumentNumber>
  <glDescription>string</glDescription>
  <glPostingDate>2019-05-23T21:00:10Z</glPostingDate>
  <fiscalYear>string</fiscalYear>
  <fiscalPeriod>string</fiscalPeriod>
  <erpFiscalPeriod>string</erpFiscalPeriod>
  <erpFiscalYear>string</erpFiscalYear>
  <establishmentCode>string</establishmentCode>
  <environmentCode>string</environmentCode>
  <nFeNumber>string</nFeNumber>
  <nfNumber>string</nfNumber>
  <nFeServiceNumber>string</nFeServiceNumber>
  <nFeServiceIndicator>string</nFeServiceIndicator>
  <totalValue>0</totalValue>
  <totalValue2>0</totalValue2>
  <seriesNumber>string</seriesNumber>
  <issuerID>string</issuerID>
  <partialDeduct>0</partialDeduct>
  <typeOfService>string</typeOfService>
  <withholdingSubContractor>0</withholdingSubContractor>
  <withholdingExemption>0</withholdingExemption>
  <services15>0</services15>
  <services20>0</services20>
  <services25>0</services25>
  <additionalWithholdingExemption>0</additionalWithholdingExemption>
  <cprbIndicator>string</cprbIndicator>
  <customerIdType>string</customerIdType>
  <creationDate>2019-05-23T21:00:10Z</creationDate>
  <creationTime>string</creationTime>
  <reversalOperation>0</reversalOperation>
  <reversalFiscalYear>0</reversalFiscalYear>
  <reversalCompanyCode>string</reversalCompanyCode>
  <reversalAccountingDocument>string</reversalAccountingDocument>
  <externalReference>string</externalReference>
  <originalLineNumberReference>string</originalLineNumberReference>
  <registrationNumber>string</registrationNumber>
  <paymentConditions>string</paymentConditions>
  <supplierFiscalRepName>string</supplierFiscalRepName>
  <supplierFiscalRepAddress>string</supplierFiscalRepAddress>
  <supplierFiscalDescription>string</supplierFiscalDescription>
  <customerFiscalRepName>string</customerFiscalRepName>
  <customerFiscalRepAddress>string</customerFiscalRepAddress>
  <customerFiscalDescription>string</customerFiscalDescription>
  <supplierCertifiedEmail>string</supplierCertifiedEmail>
  <customerCertifiedEmail>string</customerCertifiedEmail>
  <supplierTIN>string</supplierTIN>
  <customerTIN>string</customerTIN>
  <supplierEORICode>string</supplierEORICode>
  <customerEORICode>string</customerEORICode>
  <supplierBIC>string</supplierBIC>
  <customer>
    <businessEntityID>string</businessEntityID>
    <name>string</name>
    <billToCountry>string</billToCountry>
    <vatNumberUsed>string</vatNumberUsed>
    <countryVatNumberUsed>string</countryVatNumberUsed>
    <billToStreet>string</billToStreet>
    <billToBuildingNumber>string</billToBuildingNumber>
    <billToCity>string</billToCity>
    <billToPostalCode>string</billToPostalCode>
    <ucr>string</ucr>
    <website>string</website>
    <billToAddressDetail>string</billToAddressDetail>
    <billToRegion>string</billToRegion>
    <billToStreetNumber>string</billToStreetNumber>
    <contactFirstName>string</contactFirstName>
    <contactLastName>string</contactLastName>
    <contactTitle>string</contactTitle>
    <contactVATNumber>string</contactVATNumber>
    <deliveryDate>2019-05-23T21:00:10Z</deliveryDate>
    <deliveryId>string</deliveryId>
    <emailAddress>string</emailAddress>
    <faxNumber>string</faxNumber>
    <shipFromAddressDetail>string</shipFromAddressDetail>
    <shipFromBuildingNumber>string</shipFromBuildingNumber>
    <shipFromCity>string</shipFromCity>
    <shipFromCountry>string</shipFromCountry>
    <shipFromLocationId>string</shipFromLocationId>
    <shipFromPostalCode>string</shipFromPostalCode>
    <shipFromRegion>string</shipFromRegion>
    <shipFromStreet>string</shipFromStreet>
    <shipFromStreetNumber>string</shipFromStreetNumber>
    <shipFromWarehouseId>string</shipFromWarehouseId>
    <shipToAddressDetail>string</shipToAddressDetail>
    <shipToBuildingNumber>string</shipToBuildingNumber>
    <shipToCity>string</shipToCity>
    <shipToCountry>string</shipToCountry>
    <shipToLocationId>string</shipToLocationId>
    <shipToPostalCode>string</shipToPostalCode>
    <shipToRegion>string</shipToRegion>
    <shipToStreet>string</shipToStreet>
    <shipToStreetNumber>string</shipToStreetNumber>
    <shipToWarehouseId>string</shipToWarehouseId>
    <telephoneNumber>string</telephoneNumber>
    <fiscalRepVATNumber>string</fiscalRepVATNumber>
    <idType>string</idType>
    <idNumber>string</idNumber>
    <localTaxNumber>string</localTaxNumber>
  </customer>
  <supplier>
    <invoiceNumber>string</invoiceNumber>
    <invoiceLineNumber>string</invoiceLineNumber>
    <originalInvoiceNumber>string</originalInvoiceNumber>
    <communicationType>string</communicationType>
    <businessEntityID>string</businessEntityID>
    <name>string</name>
    <billToCountry>string</billToCountry>
    <vatNumberUsed>string</vatNumberUsed>
    <countryVatNumberUsed>string</countryVatNumberUsed>
    <billToStreet>string</billToStreet>
    <billToBuildingNumber>string</billToBuildingNumber>
    <billToCity>string</billToCity>
    <billToPostalCode>string</billToPostalCode>
    <ucr>string</ucr>
    <website>string</website>
    <billToAddressDetail>string</billToAddressDetail>
    <billToRegion>string</billToRegion>
    <billToStreetNumber>string</billToStreetNumber>
    <contactFirstName>string</contactFirstName>
    <contactLastName>string</contactLastName>
    <contactTitle>string</contactTitle>
    <contactVATNumber>string</contactVATNumber>
    <deliveryDate>2019-05-23T21:00:10Z</deliveryDate>
    <deliveryId>string</deliveryId>
    <emailAddress>string</emailAddress>
    <faxNumber>string</faxNumber>
    <shipFromAddressDetail>string</shipFromAddressDetail>
    <shipFromBuildingNumber>string</shipFromBuildingNumber>
    <shipFromCity>string</shipFromCity>
    <shipFromCountry>string</shipFromCountry>
    <shipFromLocationId>string</shipFromLocationId>
    <shipFromPostalCode>string</shipFromPostalCode>
    <shipFromRegion>string</shipFromRegion>
    <shipFromStreet>string</shipFromStreet>
    <shipFromStreetNumber>string</shipFromStreetNumber>
    <shipFromWarehouseId>string</shipFromWarehouseId>
    <shipToAddressDetail>string</shipToAddressDetail>
    <shipToBuildingNumber>string</shipToBuildingNumber>
    <shipToCity>string</shipToCity>
    <shipToCountry>string</shipToCountry>
    <shipToLocationId>string</shipToLocationId>
    <shipToPostalCode>string</shipToPostalCode>
    <shipToRegion>string</shipToRegion>
    <shipToStreet>string</shipToStreet>
    <shipToStreetNumber>string</shipToStreetNumber>
    <shipToWarehouseId>string</shipToWarehouseId>
    <telephoneNumber>string</telephoneNumber>
    <fiscalRepVATNumber>string</fiscalRepVATNumber>
    <idType>string</idType>
    <idNumber>string</idNumber>
    <localTaxNumber>string</localTaxNumber>
  </supplier>
  <lines>
    <currency>string</currency>
    <currency2>string</currency2>
    <exchangeRate>0</exchangeRate>
    <vatCode>string</vatCode>
    <vatRate>string</vatRate>
    <itemDescription>string</itemDescription>
    <itemClassification>string</itemClassification>
    <taxableBasisCredit>0</taxableBasisCredit>
    <taxableBasisDebet>0</taxableBasisDebet>
    <valueVatCredit>0</valueVatCredit>
    <valueVatDebet>0</valueVatDebet>
    <totalValueLine>0</totalValueLine>
    <amountVatDeducted>0</amountVatDeducted>
    <taxableBasisCurrency2>0</taxableBasisCurrency2>
    <valueVatCurrency2>0</valueVatCurrency2>
    <totalValueLineCurrency2>0</totalValueLineCurrency2>
    <countryDispatch>string</countryDispatch>
    <countryArrival>string</countryArrival>
    <deliveryConditions>string</deliveryConditions>
    <additionalDocumentReference>string</additionalDocumentReference>
    <reportingType>string</reportingType>
    <transactionType>0</transactionType>
    <additionalTransactionType>0</additionalTransactionType>
    <intrastatCode>string</intrastatCode>
    <extrastatCode>string</extrastatCode>
    <additionalDescription>string</additionalDescription>
    <weight>0</weight>
    <unitOfMeasure>string</unitOfMeasure>
    <quantity>0</quantity>
    <additionalUnitOfMeasure>string</additionalUnitOfMeasure>
    <commercialValue>0</commercialValue>
    <statisticalValue>0</statisticalValue>
    <commercialValueCurrency2>0</commercialValueCurrency2>
    <statisticalValueCurrency2>0</statisticalValueCurrency2>
    <itemType>string</itemType>
    <modeOfTransport>0</modeOfTransport>
    <regionDispatch>string</regionDispatch>
    <harbourDispatch>string</harbourDispatch>
    <regionArrival>string</regionArrival>
    <harbourArrival>string</harbourArrival>
    <countryOrigin>string</countryOrigin>
    <purchaseExtra1>string</purchaseExtra1>
    <purchaseExtra2>string</purchaseExtra2>
    <purchaseExtra3>string</purchaseExtra3>
    <purchaseExtra4>string</purchaseExtra4>
    <purchaseExtra5>string</purchaseExtra5>
    <purchaseExtra6>string</purchaseExtra6>
    <purchaseExtra7>string</purchaseExtra7>
    <purchaseExtra8>string</purchaseExtra8>
    <purchaseExtra9>string</purchaseExtra9>
    <purchaseExtra10>string</purchaseExtra10>
    <salesExtra1>string</salesExtra1>
    <salesExtra2>string</salesExtra2>
    <salesExtra3>string</salesExtra3>
    <salesExtra4>string</salesExtra4>
    <salesExtra5>string</salesExtra5>
    <salesExtra6>string</salesExtra6>
    <salesExtra7>string</salesExtra7>
    <salesExtra8>string</salesExtra8>
    <salesExtra9>string</salesExtra9>
    <salesExtra10>string</salesExtra10>
    <mossReporterVatNumberUsed>string</mossReporterVatNumberUsed>
    <administrationCode>string</administrationCode>
    <vatCodeAssignerCode>string</vatCodeAssignerCode>
    <isOriginal>true</isOriginal>
    <deliveryConditionsPlace>string</deliveryConditionsPlace>
    <regionOrigin>string</regionOrigin>
    <vatCodeAccountingKey>string</vatCodeAccountingKey>
    <originalTaxRateApplied>string</originalTaxRateApplied>
    <originalVatcodeUsed>string</originalVatcodeUsed>
    <originalVatcodeUsedDescription>string</originalVatcodeUsedDescription>
    <vatGlAccountCredit>string</vatGlAccountCredit>
    <vatGlAccountDebet>string</vatGlAccountDebet>
    <vatGlAccountPurchases>string</vatGlAccountPurchases>
    <vatGlAccountSales>string</vatGlAccountSales>
    <revenuesGlAccount>string</revenuesGlAccount>
    <costsGlAccount>string</costsGlAccount>
    <plantCode>string</plantCode>
    <materialTaxClassification>string</materialTaxClassification>
    <customerTaxClassification>string</customerTaxClassification>
    <invoiceLineNumber>string</invoiceLineNumber>
    <unitPrice>0</unitPrice>
    <creditNoteReason>string</creditNoteReason>
    <generalLedgerId>string</generalLedgerId>
    <generalLedgerType>string</generalLedgerType>
    <journalDescription>string</journalDescription>
    <journalId>string</journalId>
    <journalType>string</journalType>
    <statisticalProcedure>string</statisticalProcedure>
    <propertyCode>string</propertyCode>
    <propertyRegisterReference>string</propertyRegisterReference>
    <exemptReasonCode>string</exemptReasonCode>
    <utilizationDate>2019-05-23T21:00:10Z</utilizationDate>
    <annualProrate>0</annualProrate>
    <annualDeduction>0</annualDeduction>
    <annualDeductionEffectiveDate>2019-05-23T21:00:10Z</annualDeductionEffectiveDate>
    <assetId>string</assetId>
    <deliveryIdentification>string</deliveryIdentification>
    <firstSemester>true</firstSemester>
    <withholdingAmount>0</withholdingAmount>
    <operationType>string</operationType>
    <profitCenter>string</profitCenter>
    <discountBaseAmount>0</discountBaseAmount>
    <businessArea>string</businessArea>
    <costCenter>string</costCenter>
    <materialNumber>string</materialNumber>
    <assignmentNumber>string</assignmentNumber>
    <projectNumber>string</projectNumber>
    <establishmentCode>string</establishmentCode>
    <creationDate>2019-05-23T21:00:10Z</creationDate>
    <creationTime>string</creationTime>
    <exchangeRate2>0</exchangeRate2>
    <withholdingType>string</withholdingType>
    <withholdingRate>0</withholdingRate>
    <withholdingDescription>string</withholdingDescription>
    <salesOrderDate>2019-05-23T21:00:10Z</salesOrderDate>
    <salesOrderNumber>string</salesOrderNumber>
    <purchaseOrderNumber>string</purchaseOrderNumber>
    <shipperCountryVATNumber>string</shipperCountryVATNumber>
    <shipperCountryVATNumberUsed>string</shipperCountryVATNumberUsed>
    <shipperName>string</shipperName>
    <shipperLocalCode>string</shipperLocalCode>
    <shipmentType>string</shipmentType>
    <shipmentDescription>string</shipmentDescription>
    <shipmentWeightUOM>string</shipmentWeightUOM>
    <shipmentWeightGross>0</shipmentWeightGross>
    <shipmentWeightNet>0</shipmentWeightNet>
    <shipmentDateTime>2019-05-23T21:00:10Z</shipmentDateTime>
    <itemCodeType>string</itemCodeType>
    <itemCode>string</itemCode>
    <transactionEndDate>2019-05-23T21:00:10Z</transactionEndDate>
    <paymentExpireDate>2019-05-23T21:00:10Z</paymentExpireDate>
    <paymentBankName>string</paymentBankName>
    <paymentCode>string</paymentCode>
    <intBankAccountNumber>string</intBankAccountNumber>
    <originalInvoiceDate>2019-05-23T21:00:10Z</originalInvoiceDate>
    <shipmentNumofPackages>0</shipmentNumofPackages>
    <paymentDueDate>0</paymentDueDate>
    <vatDueDate>string</vatDueDate>
    <virtualStamp>string</virtualStamp>
    <stampAmount>0</stampAmount>
    <reaOffice>string</reaOffice>
    <reaNumber>string</reaNumber>
    <socialCapital>0</socialCapital>
    <soleShareholder>string</soleShareholder>
    <statusLiquidation>string</statusLiquidation>
    <referenceProvision>string</referenceProvision>
    <doacupCode>string</doacupCode>
    <doacigCode>string</doacigCode>
    <dtCtrDocumentID>string</dtCtrDocumentID>
    <dtCtrDate>2019-05-23T21:00:10Z</dtCtrDate>
    <dtCtrItemNum>string</dtCtrItemNum>
    <dtCtrConvCode>string</dtCtrConvCode>
    <dtCtrCUPCode>string</dtCtrCUPCode>
    <dtCtrCIGCode>string</dtCtrCIGCode>
    <dtCnvDocumentID>string</dtCnvDocumentID>
    <dtCnvDate>2019-05-23T21:00:10Z</dtCnvDate>
    <dtCnvItemNum>string</dtCnvItemNum>
    <dtCnvConvCode>string</dtCnvConvCode>
    <dtCnvCUPCode>string</dtCnvCUPCode>
    <dtCnvCIGCode>string</dtCnvCIGCode>
    <dtRczDocumentID>string</dtRczDocumentID>
    <dtRczDate>2019-05-23T21:00:10Z</dtRczDate>
    <dtRczItemNum>string</dtRczItemNum>
    <dtRczConvCode>string</dtRczConvCode>
    <dtRczCUPCode>string</dtRczCUPCode>
    <dtRczCIGCode>string</dtRczCIGCode>
    <adGestionaliType>string</adGestionaliType>
    <adGestionaliText>string</adGestionaliText>
    <adGestionaliNumber>0</adGestionaliNumber>
    <adGestionaliDate>2019-05-23T21:00:10Z</adGestionaliDate>
    <adGestionaliType2>string</adGestionaliType2>
    <adGestionaliText2>string</adGestionaliText2>
    <adGestionaliType3>string</adGestionaliType3>
    <adGestionaliText3>string</adGestionaliText3>
    <adGestionaliType4>string</adGestionaliType4>
    <adGestionaliText4>string</adGestionaliText4>
    <adGestionaliType5>string</adGestionaliType5>
    <adGestionaliText5>string</adGestionaliText5>
    <lineNature>string</lineNature>
    <lineAdminReference>string</lineAdminReference>
    <shipmentCause>string</shipmentCause>
    <shipTimeStamp>2019-05-23T21:00:10Z</shipTimeStamp>
    <shipmentStartDate>2019-05-23T21:00:10Z</shipmentStartDate>
    <alboProfessional>string</alboProfessional>
    <alboProvince>string</alboProvince>
    <alboInscriptionDate>2019-05-23T21:00:10Z</alboInscriptionDate>
    <supplierLocalOfficeAddress>string</supplierLocalOfficeAddress>
    <supplierLocalOfficeStreetNumber>string</supplierLocalOfficeStreetNumber>
    <supplierLocalOfficePostalCode>0</supplierLocalOfficePostalCode>
    <supplierLocalOfficeCity>string</supplierLocalOfficeCity>
    <supplierLocalOfficeProvince>string</supplierLocalOfficeProvince>
    <supplierLocalOfficeCountry>string</supplierLocalOfficeCountry>
    <supplierFiscalRepName>string</supplierFiscalRepName>
    <supplierFiscalRepTIN>string</supplierFiscalRepTIN>
    <supplierFiscalRepFirstName>string</supplierFiscalRepFirstName>
    <supplierFiscalRepLastName>string</supplierFiscalRepLastName>
    <supplierFiscalRepCodEORI>string</supplierFiscalRepCodEORI>
    <customerLocalOfficeAddress>string</customerLocalOfficeAddress>
    <customerLocalOfficeStreetNumber>string</customerLocalOfficeStreetNumber>
    <customerLocalOfficePostalCode>0</customerLocalOfficePostalCode>
    <customerLocalOfficeCity>string</customerLocalOfficeCity>
    <customerLocalOfficeProvince>string</customerLocalOfficeProvince>
    <customerLocalOfficeCountry>string</customerLocalOfficeCountry>
    <customerFiscalRepFirstName>string</customerFiscalRepFirstName>
    <customerFiscalRepLastName>string</customerFiscalRepLastName>
    <roundingAmount>0</roundingAmount>
    <socSecType>string</socSecType>
    <socSecRate>0</socSecRate>
    <socSecContributionAmount>0</socSecContributionAmount>
    <socSecTaxableAmount>0</socSecTaxableAmount>
    <socSecVATRate>0</socSecVATRate>
    <socSecWithheld>string</socSecWithheld>
    <socSecNatura>string</socSecNatura>
    <socSecAdminReference>string</socSecAdminReference>
    <art73>string</art73>
    <stageReference>0</stageReference>
    <shipperTIN>string</shipperTIN>
    <driverFirstName>string</driverFirstName>
    <driverLastName>string</driverLastName>
    <resaType>string</resaType>
    <mainInvoiceNumber>string</mainInvoiceNumber>
    <mainInvoiceDate>2019-05-23T21:00:10Z</mainInvoiceDate>
    <subjectWithheld>string</subjectWithheld>
    <additionalExpenses>0</additionalExpenses>
    <paymentRoundingAmount>0</paymentRoundingAmount>
    <vehicleRegistrationDate>2019-05-23T21:00:10Z</vehicleRegistrationDate>
    <vehicleTotalTravel>string</vehicleTotalTravel>
    <paymentBeneficiary>string</paymentBeneficiary>
    <officePostalCode>string</officePostalCode>
    <signerLastName>string</signerLastName>
    <signerFirstName>string</signerFirstName>
    <signerTIN>string</signerTIN>
    <abiCode>0</abiCode>
    <cabCode>0</cabCode>
    <prepaymentDiscount>0</prepaymentDiscount>
    <prepaymentDueDate>2019-05-23T21:00:10Z</prepaymentDueDate>
    <penaltyLatePayment>0</penaltyLatePayment>
    <penaltyStartDate>2019-05-23T21:00:10Z</penaltyStartDate>
    <supplierFiscalRepTitle>string</supplierFiscalRepTitle>
    <driverTitle>string</driverTitle>
    <doaNumItem>string</doaNumItem>
    <supplierFiscalRepCountryVATNumber>string</supplierFiscalRepCountryVATNumber>
    <customerFiscalRepCountryVATNumber>string</customerFiscalRepCountryVATNumber>
    <salesOrderNumber2>string</salesOrderNumber2>
    <salesOrderNumber3>string</salesOrderNumber3>
    <salesOrderNumber4>string</salesOrderNumber4>
    <salesOrderNumber5>string</salesOrderNumber5>
  </lines>
</ApiTransaction>
```

<section>
<h3 id="transactions_index-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ApiTransaction](#schemaapitransaction)|true|none|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="transactions_index-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="transactions_index-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

<section>

## Creates transactions

<a id="opIdTransactions_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://uatvat-api.sovos.com/api/transactions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://uatvat-api.sovos.com/api/transactions HTTP/1.1
Host: uatvat-api.sovos.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "importProfileName": "string",
  "fileName": "string",
  "customValues": {
    "property1": "string",
    "property2": "string"
  },
  "transactions": [
    {
      "companyCode": "string",
      "invoiceNumber": "string",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "originalInvoiceNumber": "string",
      "currentApprovalStatus": "string",
      "documentType": "string",
      "sequencialNumberSalesBook": "string",
      "sequencialNumberPurchaseBook": "string",
      "transactionDate": "2019-05-23T21:00:10Z",
      "intrastatDate": "2019-05-23T21:00:10Z",
      "invoiceDate": "2019-05-23T21:00:10Z",
      "paymentDate": "2019-05-23T21:00:10Z",
      "reportDate": "2019-05-23T21:00:10Z",
      "invoiceType": "string",
      "invoiceCorrectionType": "string",
      "invoiceSelfBilled": true,
      "taxRegimeSales": "string",
      "taxRegimePurchases": "string",
      "customsNumber": "string",
      "customsDate": "2019-05-23T21:00:10Z",
      "paymentMethod": "string",
      "bankAccount": "string",
      "transactionCode": "string",
      "customsValue": "string",
      "erpDocument": "string",
      "referenceId": "string",
      "creditIndicator": "string",
      "lastInvoiceNumber": "string",
      "transactionIsDeleted": true,
      "accountingDocumentNumber": "string",
      "glDescription": "string",
      "glPostingDate": "2019-05-23T21:00:10Z",
      "fiscalYear": "string",
      "fiscalPeriod": "string",
      "erpFiscalPeriod": "string",
      "erpFiscalYear": "string",
      "establishmentCode": "string",
      "environmentCode": "string",
      "nFeNumber": "string",
      "nfNumber": "string",
      "nFeServiceNumber": "string",
      "nFeServiceIndicator": "string",
      "totalValue": 0,
      "totalValue2": 0,
      "seriesNumber": "string",
      "issuerID": "string",
      "partialDeduct": 0,
      "typeOfService": "string",
      "withholdingSubContractor": 0,
      "withholdingExemption": 0,
      "services15": 0,
      "services20": 0,
      "services25": 0,
      "additionalWithholdingExemption": 0,
      "cprbIndicator": "string",
      "customerIdType": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "reversalOperation": 0,
      "reversalFiscalYear": 0,
      "reversalCompanyCode": "string",
      "reversalAccountingDocument": "string",
      "externalReference": "string",
      "originalLineNumberReference": "string",
      "registrationNumber": "string",
      "paymentConditions": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepAddress": "string",
      "supplierFiscalDescription": "string",
      "customerFiscalRepName": "string",
      "customerFiscalRepAddress": "string",
      "customerFiscalDescription": "string",
      "supplierCertifiedEmail": "string",
      "customerCertifiedEmail": "string",
      "supplierTIN": "string",
      "customerTIN": "string",
      "supplierEORICode": "string",
      "customerEORICode": "string",
      "supplierBIC": "string",
      "customer": {
        "businessEntityID": "string",
        "name": "string",
        "billToCountry": "string",
        "vatNumberUsed": "string",
        "countryVatNumberUsed": "string",
        "billToStreet": "string",
        "billToBuildingNumber": "string",
        "billToCity": "string",
        "billToPostalCode": "string",
        "ucr": "string",
        "website": "string",
        "billToAddressDetail": "string",
        "billToRegion": "string",
        "billToStreetNumber": "string",
        "contactFirstName": "string",
        "contactLastName": "string",
        "contactTitle": "string",
        "contactVATNumber": "string",
        "deliveryDate": "2019-05-23T21:00:10Z",
        "deliveryId": "string",
        "emailAddress": "string",
        "faxNumber": "string",
        "shipFromAddressDetail": "string",
        "shipFromBuildingNumber": "string",
        "shipFromCity": "string",
        "shipFromCountry": "string",
        "shipFromLocationId": "string",
        "shipFromPostalCode": "string",
        "shipFromRegion": "string",
        "shipFromStreet": "string",
        "shipFromStreetNumber": "string",
        "shipFromWarehouseId": "string",
        "shipToAddressDetail": "string",
        "shipToBuildingNumber": "string",
        "shipToCity": "string",
        "shipToCountry": "string",
        "shipToLocationId": "string",
        "shipToPostalCode": "string",
        "shipToRegion": "string",
        "shipToStreet": "string",
        "shipToStreetNumber": "string",
        "shipToWarehouseId": "string",
        "telephoneNumber": "string",
        "fiscalRepVATNumber": "string",
        "idType": "string",
        "idNumber": "string",
        "localTaxNumber": "string"
      },
      "supplier": {
        "invoiceNumber": "string",
        "invoiceLineNumber": "string",
        "originalInvoiceNumber": "string",
        "communicationType": "string",
        "businessEntityID": "string",
        "name": "string",
        "billToCountry": "string",
        "vatNumberUsed": "string",
        "countryVatNumberUsed": "string",
        "billToStreet": "string",
        "billToBuildingNumber": "string",
        "billToCity": "string",
        "billToPostalCode": "string",
        "ucr": "string",
        "website": "string",
        "billToAddressDetail": "string",
        "billToRegion": "string",
        "billToStreetNumber": "string",
        "contactFirstName": "string",
        "contactLastName": "string",
        "contactTitle": "string",
        "contactVATNumber": "string",
        "deliveryDate": "2019-05-23T21:00:10Z",
        "deliveryId": "string",
        "emailAddress": "string",
        "faxNumber": "string",
        "shipFromAddressDetail": "string",
        "shipFromBuildingNumber": "string",
        "shipFromCity": "string",
        "shipFromCountry": "string",
        "shipFromLocationId": "string",
        "shipFromPostalCode": "string",
        "shipFromRegion": "string",
        "shipFromStreet": "string",
        "shipFromStreetNumber": "string",
        "shipFromWarehouseId": "string",
        "shipToAddressDetail": "string",
        "shipToBuildingNumber": "string",
        "shipToCity": "string",
        "shipToCountry": "string",
        "shipToLocationId": "string",
        "shipToPostalCode": "string",
        "shipToRegion": "string",
        "shipToStreet": "string",
        "shipToStreetNumber": "string",
        "shipToWarehouseId": "string",
        "telephoneNumber": "string",
        "fiscalRepVATNumber": "string",
        "idType": "string",
        "idNumber": "string",
        "localTaxNumber": "string"
      },
      "lines": [
        {
          "currency": "string",
          "currency2": "string",
          "exchangeRate": 0,
          "vatCode": "string",
          "vatRate": "string",
          "itemDescription": "string",
          "itemClassification": "string",
          "taxableBasisCredit": 0,
          "taxableBasisDebet": 0,
          "valueVatCredit": 0,
          "valueVatDebet": 0,
          "totalValueLine": 0,
          "amountVatDeducted": 0,
          "taxableBasisCurrency2": 0,
          "valueVatCurrency2": 0,
          "totalValueLineCurrency2": 0,
          "countryDispatch": "string",
          "countryArrival": "string",
          "deliveryConditions": "string",
          "additionalDocumentReference": "string",
          "reportingType": "string",
          "transactionType": 0,
          "additionalTransactionType": 0,
          "intrastatCode": "string",
          "extrastatCode": "string",
          "additionalDescription": "string",
          "weight": 0,
          "unitOfMeasure": "string",
          "quantity": 0,
          "additionalUnitOfMeasure": "string",
          "commercialValue": 0,
          "statisticalValue": 0,
          "commercialValueCurrency2": 0,
          "statisticalValueCurrency2": 0,
          "itemType": "string",
          "modeOfTransport": 0,
          "regionDispatch": "string",
          "harbourDispatch": "string",
          "regionArrival": "string",
          "harbourArrival": "string",
          "countryOrigin": "string",
          "purchaseExtra1": "string",
          "purchaseExtra2": "string",
          "purchaseExtra3": "string",
          "purchaseExtra4": "string",
          "purchaseExtra5": "string",
          "purchaseExtra6": "string",
          "purchaseExtra7": "string",
          "purchaseExtra8": "string",
          "purchaseExtra9": "string",
          "purchaseExtra10": "string",
          "salesExtra1": "string",
          "salesExtra2": "string",
          "salesExtra3": "string",
          "salesExtra4": "string",
          "salesExtra5": "string",
          "salesExtra6": "string",
          "salesExtra7": "string",
          "salesExtra8": "string",
          "salesExtra9": "string",
          "salesExtra10": "string",
          "mossReporterVatNumberUsed": "string",
          "administrationCode": "string",
          "vatCodeAssignerCode": "string",
          "isOriginal": true,
          "deliveryConditionsPlace": "string",
          "regionOrigin": "string",
          "vatCodeAccountingKey": "string",
          "originalTaxRateApplied": "string",
          "originalVatcodeUsed": "string",
          "originalVatcodeUsedDescription": "string",
          "vatGlAccountCredit": "string",
          "vatGlAccountDebet": "string",
          "vatGlAccountPurchases": "string",
          "vatGlAccountSales": "string",
          "revenuesGlAccount": "string",
          "costsGlAccount": "string",
          "plantCode": "string",
          "materialTaxClassification": "string",
          "customerTaxClassification": "string",
          "invoiceLineNumber": "string",
          "unitPrice": 0,
          "creditNoteReason": "string",
          "generalLedgerId": "string",
          "generalLedgerType": "string",
          "journalDescription": "string",
          "journalId": "string",
          "journalType": "string",
          "statisticalProcedure": "string",
          "propertyCode": "string",
          "propertyRegisterReference": "string",
          "exemptReasonCode": "string",
          "utilizationDate": "2019-05-23T21:00:10Z",
          "annualProrate": 0,
          "annualDeduction": 0,
          "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
          "assetId": "string",
          "deliveryIdentification": "string",
          "firstSemester": true,
          "withholdingAmount": 0,
          "operationType": "string",
          "profitCenter": "string",
          "discountBaseAmount": 0,
          "businessArea": "string",
          "costCenter": "string",
          "materialNumber": "string",
          "assignmentNumber": "string",
          "projectNumber": "string",
          "establishmentCode": "string",
          "creationDate": "2019-05-23T21:00:10Z",
          "creationTime": "string",
          "exchangeRate2": 0,
          "withholdingType": "string",
          "withholdingRate": 0,
          "withholdingDescription": "string",
          "salesOrderDate": "2019-05-23T21:00:10Z",
          "salesOrderNumber": "string",
          "purchaseOrderNumber": "string",
          "shipperCountryVATNumber": "string",
          "shipperCountryVATNumberUsed": "string",
          "shipperName": "string",
          "shipperLocalCode": "string",
          "shipmentType": "string",
          "shipmentDescription": "string",
          "shipmentWeightUOM": "string",
          "shipmentWeightGross": 0,
          "shipmentWeightNet": 0,
          "shipmentDateTime": "2019-05-23T21:00:10Z",
          "itemCodeType": "string",
          "itemCode": "string",
          "transactionEndDate": "2019-05-23T21:00:10Z",
          "paymentExpireDate": "2019-05-23T21:00:10Z",
          "paymentBankName": "string",
          "paymentCode": "string",
          "intBankAccountNumber": "string",
          "originalInvoiceDate": "2019-05-23T21:00:10Z",
          "shipmentNumofPackages": 0,
          "paymentDueDate": 0,
          "vatDueDate": "string",
          "virtualStamp": "string",
          "stampAmount": 0,
          "reaOffice": "string",
          "reaNumber": "string",
          "socialCapital": 0,
          "soleShareholder": "string",
          "statusLiquidation": "string",
          "referenceProvision": "string",
          "doacupCode": "string",
          "doacigCode": "string",
          "dtCtrDocumentID": "string",
          "dtCtrDate": "2019-05-23T21:00:10Z",
          "dtCtrItemNum": "string",
          "dtCtrConvCode": "string",
          "dtCtrCUPCode": "string",
          "dtCtrCIGCode": "string",
          "dtCnvDocumentID": "string",
          "dtCnvDate": "2019-05-23T21:00:10Z",
          "dtCnvItemNum": "string",
          "dtCnvConvCode": "string",
          "dtCnvCUPCode": "string",
          "dtCnvCIGCode": "string",
          "dtRczDocumentID": "string",
          "dtRczDate": "2019-05-23T21:00:10Z",
          "dtRczItemNum": "string",
          "dtRczConvCode": "string",
          "dtRczCUPCode": "string",
          "dtRczCIGCode": "string",
          "adGestionaliType": "string",
          "adGestionaliText": "string",
          "adGestionaliNumber": 0,
          "adGestionaliDate": "2019-05-23T21:00:10Z",
          "adGestionaliType2": "string",
          "adGestionaliText2": "string",
          "adGestionaliType3": "string",
          "adGestionaliText3": "string",
          "adGestionaliType4": "string",
          "adGestionaliText4": "string",
          "adGestionaliType5": "string",
          "adGestionaliText5": "string",
          "lineNature": "string",
          "lineAdminReference": "string",
          "shipmentCause": "string",
          "shipTimeStamp": "2019-05-23T21:00:10Z",
          "shipmentStartDate": "2019-05-23T21:00:10Z",
          "alboProfessional": "string",
          "alboProvince": "string",
          "alboInscriptionDate": "2019-05-23T21:00:10Z",
          "supplierLocalOfficeAddress": "string",
          "supplierLocalOfficeStreetNumber": "string",
          "supplierLocalOfficePostalCode": 0,
          "supplierLocalOfficeCity": "string",
          "supplierLocalOfficeProvince": "string",
          "supplierLocalOfficeCountry": "string",
          "supplierFiscalRepName": "string",
          "supplierFiscalRepTIN": "string",
          "supplierFiscalRepFirstName": "string",
          "supplierFiscalRepLastName": "string",
          "supplierFiscalRepCodEORI": "string",
          "customerLocalOfficeAddress": "string",
          "customerLocalOfficeStreetNumber": "string",
          "customerLocalOfficePostalCode": 0,
          "customerLocalOfficeCity": "string",
          "customerLocalOfficeProvince": "string",
          "customerLocalOfficeCountry": "string",
          "customerFiscalRepFirstName": "string",
          "customerFiscalRepLastName": "string",
          "roundingAmount": 0,
          "socSecType": "string",
          "socSecRate": 0,
          "socSecContributionAmount": 0,
          "socSecTaxableAmount": 0,
          "socSecVATRate": 0,
          "socSecWithheld": "string",
          "socSecNatura": "string",
          "socSecAdminReference": "string",
          "art73": "string",
          "stageReference": 0,
          "shipperTIN": "string",
          "driverFirstName": "string",
          "driverLastName": "string",
          "resaType": "string",
          "mainInvoiceNumber": "string",
          "mainInvoiceDate": "2019-05-23T21:00:10Z",
          "subjectWithheld": "string",
          "additionalExpenses": 0,
          "paymentRoundingAmount": 0,
          "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
          "vehicleTotalTravel": "string",
          "paymentBeneficiary": "string",
          "officePostalCode": "string",
          "signerLastName": "string",
          "signerFirstName": "string",
          "signerTIN": "string",
          "abiCode": 0,
          "cabCode": 0,
          "prepaymentDiscount": 0,
          "prepaymentDueDate": "2019-05-23T21:00:10Z",
          "penaltyLatePayment": 0,
          "penaltyStartDate": "2019-05-23T21:00:10Z",
          "supplierFiscalRepTitle": "string",
          "driverTitle": "string",
          "doaNumItem": "string",
          "supplierFiscalRepCountryVATNumber": "string",
          "customerFiscalRepCountryVATNumber": "string",
          "salesOrderNumber2": "string",
          "salesOrderNumber3": "string",
          "salesOrderNumber4": "string",
          "salesOrderNumber5": "string"
        }
      ]
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/transactions',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://uatvat-api.sovos.com/api/transactions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://uatvat-api.sovos.com/api/transactions', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://uatvat-api.sovos.com/api/transactions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/transactions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://uatvat-api.sovos.com/api/transactions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/transactions`

> Body parameter

```json
{
  "importProfileName": "string",
  "fileName": "string",
  "customValues": {
    "property1": "string",
    "property2": "string"
  },
  "transactions": [
    {
      "companyCode": "string",
      "invoiceNumber": "string",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "originalInvoiceNumber": "string",
      "currentApprovalStatus": "string",
      "documentType": "string",
      "sequencialNumberSalesBook": "string",
      "sequencialNumberPurchaseBook": "string",
      "transactionDate": "2019-05-23T21:00:10Z",
      "intrastatDate": "2019-05-23T21:00:10Z",
      "invoiceDate": "2019-05-23T21:00:10Z",
      "paymentDate": "2019-05-23T21:00:10Z",
      "reportDate": "2019-05-23T21:00:10Z",
      "invoiceType": "string",
      "invoiceCorrectionType": "string",
      "invoiceSelfBilled": true,
      "taxRegimeSales": "string",
      "taxRegimePurchases": "string",
      "customsNumber": "string",
      "customsDate": "2019-05-23T21:00:10Z",
      "paymentMethod": "string",
      "bankAccount": "string",
      "transactionCode": "string",
      "customsValue": "string",
      "erpDocument": "string",
      "referenceId": "string",
      "creditIndicator": "string",
      "lastInvoiceNumber": "string",
      "transactionIsDeleted": true,
      "accountingDocumentNumber": "string",
      "glDescription": "string",
      "glPostingDate": "2019-05-23T21:00:10Z",
      "fiscalYear": "string",
      "fiscalPeriod": "string",
      "erpFiscalPeriod": "string",
      "erpFiscalYear": "string",
      "establishmentCode": "string",
      "environmentCode": "string",
      "nFeNumber": "string",
      "nfNumber": "string",
      "nFeServiceNumber": "string",
      "nFeServiceIndicator": "string",
      "totalValue": 0,
      "totalValue2": 0,
      "seriesNumber": "string",
      "issuerID": "string",
      "partialDeduct": 0,
      "typeOfService": "string",
      "withholdingSubContractor": 0,
      "withholdingExemption": 0,
      "services15": 0,
      "services20": 0,
      "services25": 0,
      "additionalWithholdingExemption": 0,
      "cprbIndicator": "string",
      "customerIdType": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "reversalOperation": 0,
      "reversalFiscalYear": 0,
      "reversalCompanyCode": "string",
      "reversalAccountingDocument": "string",
      "externalReference": "string",
      "originalLineNumberReference": "string",
      "registrationNumber": "string",
      "paymentConditions": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepAddress": "string",
      "supplierFiscalDescription": "string",
      "customerFiscalRepName": "string",
      "customerFiscalRepAddress": "string",
      "customerFiscalDescription": "string",
      "supplierCertifiedEmail": "string",
      "customerCertifiedEmail": "string",
      "supplierTIN": "string",
      "customerTIN": "string",
      "supplierEORICode": "string",
      "customerEORICode": "string",
      "supplierBIC": "string",
      "customer": {
        "businessEntityID": "string",
        "name": "string",
        "billToCountry": "string",
        "vatNumberUsed": "string",
        "countryVatNumberUsed": "string",
        "billToStreet": "string",
        "billToBuildingNumber": "string",
        "billToCity": "string",
        "billToPostalCode": "string",
        "ucr": "string",
        "website": "string",
        "billToAddressDetail": "string",
        "billToRegion": "string",
        "billToStreetNumber": "string",
        "contactFirstName": "string",
        "contactLastName": "string",
        "contactTitle": "string",
        "contactVATNumber": "string",
        "deliveryDate": "2019-05-23T21:00:10Z",
        "deliveryId": "string",
        "emailAddress": "string",
        "faxNumber": "string",
        "shipFromAddressDetail": "string",
        "shipFromBuildingNumber": "string",
        "shipFromCity": "string",
        "shipFromCountry": "string",
        "shipFromLocationId": "string",
        "shipFromPostalCode": "string",
        "shipFromRegion": "string",
        "shipFromStreet": "string",
        "shipFromStreetNumber": "string",
        "shipFromWarehouseId": "string",
        "shipToAddressDetail": "string",
        "shipToBuildingNumber": "string",
        "shipToCity": "string",
        "shipToCountry": "string",
        "shipToLocationId": "string",
        "shipToPostalCode": "string",
        "shipToRegion": "string",
        "shipToStreet": "string",
        "shipToStreetNumber": "string",
        "shipToWarehouseId": "string",
        "telephoneNumber": "string",
        "fiscalRepVATNumber": "string",
        "idType": "string",
        "idNumber": "string",
        "localTaxNumber": "string"
      },
      "supplier": {
        "invoiceNumber": "string",
        "invoiceLineNumber": "string",
        "originalInvoiceNumber": "string",
        "communicationType": "string",
        "businessEntityID": "string",
        "name": "string",
        "billToCountry": "string",
        "vatNumberUsed": "string",
        "countryVatNumberUsed": "string",
        "billToStreet": "string",
        "billToBuildingNumber": "string",
        "billToCity": "string",
        "billToPostalCode": "string",
        "ucr": "string",
        "website": "string",
        "billToAddressDetail": "string",
        "billToRegion": "string",
        "billToStreetNumber": "string",
        "contactFirstName": "string",
        "contactLastName": "string",
        "contactTitle": "string",
        "contactVATNumber": "string",
        "deliveryDate": "2019-05-23T21:00:10Z",
        "deliveryId": "string",
        "emailAddress": "string",
        "faxNumber": "string",
        "shipFromAddressDetail": "string",
        "shipFromBuildingNumber": "string",
        "shipFromCity": "string",
        "shipFromCountry": "string",
        "shipFromLocationId": "string",
        "shipFromPostalCode": "string",
        "shipFromRegion": "string",
        "shipFromStreet": "string",
        "shipFromStreetNumber": "string",
        "shipFromWarehouseId": "string",
        "shipToAddressDetail": "string",
        "shipToBuildingNumber": "string",
        "shipToCity": "string",
        "shipToCountry": "string",
        "shipToLocationId": "string",
        "shipToPostalCode": "string",
        "shipToRegion": "string",
        "shipToStreet": "string",
        "shipToStreetNumber": "string",
        "shipToWarehouseId": "string",
        "telephoneNumber": "string",
        "fiscalRepVATNumber": "string",
        "idType": "string",
        "idNumber": "string",
        "localTaxNumber": "string"
      },
      "lines": [
        {
          "currency": "string",
          "currency2": "string",
          "exchangeRate": 0,
          "vatCode": "string",
          "vatRate": "string",
          "itemDescription": "string",
          "itemClassification": "string",
          "taxableBasisCredit": 0,
          "taxableBasisDebet": 0,
          "valueVatCredit": 0,
          "valueVatDebet": 0,
          "totalValueLine": 0,
          "amountVatDeducted": 0,
          "taxableBasisCurrency2": 0,
          "valueVatCurrency2": 0,
          "totalValueLineCurrency2": 0,
          "countryDispatch": "string",
          "countryArrival": "string",
          "deliveryConditions": "string",
          "additionalDocumentReference": "string",
          "reportingType": "string",
          "transactionType": 0,
          "additionalTransactionType": 0,
          "intrastatCode": "string",
          "extrastatCode": "string",
          "additionalDescription": "string",
          "weight": 0,
          "unitOfMeasure": "string",
          "quantity": 0,
          "additionalUnitOfMeasure": "string",
          "commercialValue": 0,
          "statisticalValue": 0,
          "commercialValueCurrency2": 0,
          "statisticalValueCurrency2": 0,
          "itemType": "string",
          "modeOfTransport": 0,
          "regionDispatch": "string",
          "harbourDispatch": "string",
          "regionArrival": "string",
          "harbourArrival": "string",
          "countryOrigin": "string",
          "purchaseExtra1": "string",
          "purchaseExtra2": "string",
          "purchaseExtra3": "string",
          "purchaseExtra4": "string",
          "purchaseExtra5": "string",
          "purchaseExtra6": "string",
          "purchaseExtra7": "string",
          "purchaseExtra8": "string",
          "purchaseExtra9": "string",
          "purchaseExtra10": "string",
          "salesExtra1": "string",
          "salesExtra2": "string",
          "salesExtra3": "string",
          "salesExtra4": "string",
          "salesExtra5": "string",
          "salesExtra6": "string",
          "salesExtra7": "string",
          "salesExtra8": "string",
          "salesExtra9": "string",
          "salesExtra10": "string",
          "mossReporterVatNumberUsed": "string",
          "administrationCode": "string",
          "vatCodeAssignerCode": "string",
          "isOriginal": true,
          "deliveryConditionsPlace": "string",
          "regionOrigin": "string",
          "vatCodeAccountingKey": "string",
          "originalTaxRateApplied": "string",
          "originalVatcodeUsed": "string",
          "originalVatcodeUsedDescription": "string",
          "vatGlAccountCredit": "string",
          "vatGlAccountDebet": "string",
          "vatGlAccountPurchases": "string",
          "vatGlAccountSales": "string",
          "revenuesGlAccount": "string",
          "costsGlAccount": "string",
          "plantCode": "string",
          "materialTaxClassification": "string",
          "customerTaxClassification": "string",
          "invoiceLineNumber": "string",
          "unitPrice": 0,
          "creditNoteReason": "string",
          "generalLedgerId": "string",
          "generalLedgerType": "string",
          "journalDescription": "string",
          "journalId": "string",
          "journalType": "string",
          "statisticalProcedure": "string",
          "propertyCode": "string",
          "propertyRegisterReference": "string",
          "exemptReasonCode": "string",
          "utilizationDate": "2019-05-23T21:00:10Z",
          "annualProrate": 0,
          "annualDeduction": 0,
          "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
          "assetId": "string",
          "deliveryIdentification": "string",
          "firstSemester": true,
          "withholdingAmount": 0,
          "operationType": "string",
          "profitCenter": "string",
          "discountBaseAmount": 0,
          "businessArea": "string",
          "costCenter": "string",
          "materialNumber": "string",
          "assignmentNumber": "string",
          "projectNumber": "string",
          "establishmentCode": "string",
          "creationDate": "2019-05-23T21:00:10Z",
          "creationTime": "string",
          "exchangeRate2": 0,
          "withholdingType": "string",
          "withholdingRate": 0,
          "withholdingDescription": "string",
          "salesOrderDate": "2019-05-23T21:00:10Z",
          "salesOrderNumber": "string",
          "purchaseOrderNumber": "string",
          "shipperCountryVATNumber": "string",
          "shipperCountryVATNumberUsed": "string",
          "shipperName": "string",
          "shipperLocalCode": "string",
          "shipmentType": "string",
          "shipmentDescription": "string",
          "shipmentWeightUOM": "string",
          "shipmentWeightGross": 0,
          "shipmentWeightNet": 0,
          "shipmentDateTime": "2019-05-23T21:00:10Z",
          "itemCodeType": "string",
          "itemCode": "string",
          "transactionEndDate": "2019-05-23T21:00:10Z",
          "paymentExpireDate": "2019-05-23T21:00:10Z",
          "paymentBankName": "string",
          "paymentCode": "string",
          "intBankAccountNumber": "string",
          "originalInvoiceDate": "2019-05-23T21:00:10Z",
          "shipmentNumofPackages": 0,
          "paymentDueDate": 0,
          "vatDueDate": "string",
          "virtualStamp": "string",
          "stampAmount": 0,
          "reaOffice": "string",
          "reaNumber": "string",
          "socialCapital": 0,
          "soleShareholder": "string",
          "statusLiquidation": "string",
          "referenceProvision": "string",
          "doacupCode": "string",
          "doacigCode": "string",
          "dtCtrDocumentID": "string",
          "dtCtrDate": "2019-05-23T21:00:10Z",
          "dtCtrItemNum": "string",
          "dtCtrConvCode": "string",
          "dtCtrCUPCode": "string",
          "dtCtrCIGCode": "string",
          "dtCnvDocumentID": "string",
          "dtCnvDate": "2019-05-23T21:00:10Z",
          "dtCnvItemNum": "string",
          "dtCnvConvCode": "string",
          "dtCnvCUPCode": "string",
          "dtCnvCIGCode": "string",
          "dtRczDocumentID": "string",
          "dtRczDate": "2019-05-23T21:00:10Z",
          "dtRczItemNum": "string",
          "dtRczConvCode": "string",
          "dtRczCUPCode": "string",
          "dtRczCIGCode": "string",
          "adGestionaliType": "string",
          "adGestionaliText": "string",
          "adGestionaliNumber": 0,
          "adGestionaliDate": "2019-05-23T21:00:10Z",
          "adGestionaliType2": "string",
          "adGestionaliText2": "string",
          "adGestionaliType3": "string",
          "adGestionaliText3": "string",
          "adGestionaliType4": "string",
          "adGestionaliText4": "string",
          "adGestionaliType5": "string",
          "adGestionaliText5": "string",
          "lineNature": "string",
          "lineAdminReference": "string",
          "shipmentCause": "string",
          "shipTimeStamp": "2019-05-23T21:00:10Z",
          "shipmentStartDate": "2019-05-23T21:00:10Z",
          "alboProfessional": "string",
          "alboProvince": "string",
          "alboInscriptionDate": "2019-05-23T21:00:10Z",
          "supplierLocalOfficeAddress": "string",
          "supplierLocalOfficeStreetNumber": "string",
          "supplierLocalOfficePostalCode": 0,
          "supplierLocalOfficeCity": "string",
          "supplierLocalOfficeProvince": "string",
          "supplierLocalOfficeCountry": "string",
          "supplierFiscalRepName": "string",
          "supplierFiscalRepTIN": "string",
          "supplierFiscalRepFirstName": "string",
          "supplierFiscalRepLastName": "string",
          "supplierFiscalRepCodEORI": "string",
          "customerLocalOfficeAddress": "string",
          "customerLocalOfficeStreetNumber": "string",
          "customerLocalOfficePostalCode": 0,
          "customerLocalOfficeCity": "string",
          "customerLocalOfficeProvince": "string",
          "customerLocalOfficeCountry": "string",
          "customerFiscalRepFirstName": "string",
          "customerFiscalRepLastName": "string",
          "roundingAmount": 0,
          "socSecType": "string",
          "socSecRate": 0,
          "socSecContributionAmount": 0,
          "socSecTaxableAmount": 0,
          "socSecVATRate": 0,
          "socSecWithheld": "string",
          "socSecNatura": "string",
          "socSecAdminReference": "string",
          "art73": "string",
          "stageReference": 0,
          "shipperTIN": "string",
          "driverFirstName": "string",
          "driverLastName": "string",
          "resaType": "string",
          "mainInvoiceNumber": "string",
          "mainInvoiceDate": "2019-05-23T21:00:10Z",
          "subjectWithheld": "string",
          "additionalExpenses": 0,
          "paymentRoundingAmount": 0,
          "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
          "vehicleTotalTravel": "string",
          "paymentBeneficiary": "string",
          "officePostalCode": "string",
          "signerLastName": "string",
          "signerFirstName": "string",
          "signerTIN": "string",
          "abiCode": 0,
          "cabCode": 0,
          "prepaymentDiscount": 0,
          "prepaymentDueDate": "2019-05-23T21:00:10Z",
          "penaltyLatePayment": 0,
          "penaltyStartDate": "2019-05-23T21:00:10Z",
          "supplierFiscalRepTitle": "string",
          "driverTitle": "string",
          "doaNumItem": "string",
          "supplierFiscalRepCountryVATNumber": "string",
          "customerFiscalRepCountryVATNumber": "string",
          "salesOrderNumber2": "string",
          "salesOrderNumber3": "string",
          "salesOrderNumber4": "string",
          "salesOrderNumber5": "string"
        }
      ]
    }
  ]
}
```

```yaml
importProfileName: string
fileName: string
customValues:
  property1: string
  property2: string
transactions:
  - companyCode: string
    invoiceNumber: string
    salesOrderNumber: string
    purchaseOrderNumber: string
    originalInvoiceNumber: string
    currentApprovalStatus: string
    documentType: string
    sequencialNumberSalesBook: string
    sequencialNumberPurchaseBook: string
    transactionDate: 2019-05-23T21:00:10Z
    intrastatDate: 2019-05-23T21:00:10Z
    invoiceDate: 2019-05-23T21:00:10Z
    paymentDate: 2019-05-23T21:00:10Z
    reportDate: 2019-05-23T21:00:10Z
    invoiceType: string
    invoiceCorrectionType: string
    invoiceSelfBilled: true
    taxRegimeSales: string
    taxRegimePurchases: string
    customsNumber: string
    customsDate: 2019-05-23T21:00:10Z
    paymentMethod: string
    bankAccount: string
    transactionCode: string
    customsValue: string
    erpDocument: string
    referenceId: string
    creditIndicator: string
    lastInvoiceNumber: string
    transactionIsDeleted: true
    accountingDocumentNumber: string
    glDescription: string
    glPostingDate: 2019-05-23T21:00:10Z
    fiscalYear: string
    fiscalPeriod: string
    erpFiscalPeriod: string
    erpFiscalYear: string
    establishmentCode: string
    environmentCode: string
    nFeNumber: string
    nfNumber: string
    nFeServiceNumber: string
    nFeServiceIndicator: string
    totalValue: 0
    totalValue2: 0
    seriesNumber: string
    issuerID: string
    partialDeduct: 0
    typeOfService: string
    withholdingSubContractor: 0
    withholdingExemption: 0
    services15: 0
    services20: 0
    services25: 0
    additionalWithholdingExemption: 0
    cprbIndicator: string
    customerIdType: string
    creationDate: 2019-05-23T21:00:10Z
    creationTime: string
    reversalOperation: 0
    reversalFiscalYear: 0
    reversalCompanyCode: string
    reversalAccountingDocument: string
    externalReference: string
    originalLineNumberReference: string
    registrationNumber: string
    paymentConditions: string
    supplierFiscalRepName: string
    supplierFiscalRepAddress: string
    supplierFiscalDescription: string
    customerFiscalRepName: string
    customerFiscalRepAddress: string
    customerFiscalDescription: string
    supplierCertifiedEmail: string
    customerCertifiedEmail: string
    supplierTIN: string
    customerTIN: string
    supplierEORICode: string
    customerEORICode: string
    supplierBIC: string
    customer:
      businessEntityID: string
      name: string
      billToCountry: string
      vatNumberUsed: string
      countryVatNumberUsed: string
      billToStreet: string
      billToBuildingNumber: string
      billToCity: string
      billToPostalCode: string
      ucr: string
      website: string
      billToAddressDetail: string
      billToRegion: string
      billToStreetNumber: string
      contactFirstName: string
      contactLastName: string
      contactTitle: string
      contactVATNumber: string
      deliveryDate: 2019-05-23T21:00:10Z
      deliveryId: string
      emailAddress: string
      faxNumber: string
      shipFromAddressDetail: string
      shipFromBuildingNumber: string
      shipFromCity: string
      shipFromCountry: string
      shipFromLocationId: string
      shipFromPostalCode: string
      shipFromRegion: string
      shipFromStreet: string
      shipFromStreetNumber: string
      shipFromWarehouseId: string
      shipToAddressDetail: string
      shipToBuildingNumber: string
      shipToCity: string
      shipToCountry: string
      shipToLocationId: string
      shipToPostalCode: string
      shipToRegion: string
      shipToStreet: string
      shipToStreetNumber: string
      shipToWarehouseId: string
      telephoneNumber: string
      fiscalRepVATNumber: string
      idType: string
      idNumber: string
      localTaxNumber: string
    supplier:
      invoiceNumber: string
      invoiceLineNumber: string
      originalInvoiceNumber: string
      communicationType: string
      businessEntityID: string
      name: string
      billToCountry: string
      vatNumberUsed: string
      countryVatNumberUsed: string
      billToStreet: string
      billToBuildingNumber: string
      billToCity: string
      billToPostalCode: string
      ucr: string
      website: string
      billToAddressDetail: string
      billToRegion: string
      billToStreetNumber: string
      contactFirstName: string
      contactLastName: string
      contactTitle: string
      contactVATNumber: string
      deliveryDate: 2019-05-23T21:00:10Z
      deliveryId: string
      emailAddress: string
      faxNumber: string
      shipFromAddressDetail: string
      shipFromBuildingNumber: string
      shipFromCity: string
      shipFromCountry: string
      shipFromLocationId: string
      shipFromPostalCode: string
      shipFromRegion: string
      shipFromStreet: string
      shipFromStreetNumber: string
      shipFromWarehouseId: string
      shipToAddressDetail: string
      shipToBuildingNumber: string
      shipToCity: string
      shipToCountry: string
      shipToLocationId: string
      shipToPostalCode: string
      shipToRegion: string
      shipToStreet: string
      shipToStreetNumber: string
      shipToWarehouseId: string
      telephoneNumber: string
      fiscalRepVATNumber: string
      idType: string
      idNumber: string
      localTaxNumber: string
    lines:
      - currency: string
        currency2: string
        exchangeRate: 0
        vatCode: string
        vatRate: string
        itemDescription: string
        itemClassification: string
        taxableBasisCredit: 0
        taxableBasisDebet: 0
        valueVatCredit: 0
        valueVatDebet: 0
        totalValueLine: 0
        amountVatDeducted: 0
        taxableBasisCurrency2: 0
        valueVatCurrency2: 0
        totalValueLineCurrency2: 0
        countryDispatch: string
        countryArrival: string
        deliveryConditions: string
        additionalDocumentReference: string
        reportingType: string
        transactionType: 0
        additionalTransactionType: 0
        intrastatCode: string
        extrastatCode: string
        additionalDescription: string
        weight: 0
        unitOfMeasure: string
        quantity: 0
        additionalUnitOfMeasure: string
        commercialValue: 0
        statisticalValue: 0
        commercialValueCurrency2: 0
        statisticalValueCurrency2: 0
        itemType: string
        modeOfTransport: 0
        regionDispatch: string
        harbourDispatch: string
        regionArrival: string
        harbourArrival: string
        countryOrigin: string
        purchaseExtra1: string
        purchaseExtra2: string
        purchaseExtra3: string
        purchaseExtra4: string
        purchaseExtra5: string
        purchaseExtra6: string
        purchaseExtra7: string
        purchaseExtra8: string
        purchaseExtra9: string
        purchaseExtra10: string
        salesExtra1: string
        salesExtra2: string
        salesExtra3: string
        salesExtra4: string
        salesExtra5: string
        salesExtra6: string
        salesExtra7: string
        salesExtra8: string
        salesExtra9: string
        salesExtra10: string
        mossReporterVatNumberUsed: string
        administrationCode: string
        vatCodeAssignerCode: string
        isOriginal: true
        deliveryConditionsPlace: string
        regionOrigin: string
        vatCodeAccountingKey: string
        originalTaxRateApplied: string
        originalVatcodeUsed: string
        originalVatcodeUsedDescription: string
        vatGlAccountCredit: string
        vatGlAccountDebet: string
        vatGlAccountPurchases: string
        vatGlAccountSales: string
        revenuesGlAccount: string
        costsGlAccount: string
        plantCode: string
        materialTaxClassification: string
        customerTaxClassification: string
        invoiceLineNumber: string
        unitPrice: 0
        creditNoteReason: string
        generalLedgerId: string
        generalLedgerType: string
        journalDescription: string
        journalId: string
        journalType: string
        statisticalProcedure: string
        propertyCode: string
        propertyRegisterReference: string
        exemptReasonCode: string
        utilizationDate: 2019-05-23T21:00:10Z
        annualProrate: 0
        annualDeduction: 0
        annualDeductionEffectiveDate: 2019-05-23T21:00:10Z
        assetId: string
        deliveryIdentification: string
        firstSemester: true
        withholdingAmount: 0
        operationType: string
        profitCenter: string
        discountBaseAmount: 0
        businessArea: string
        costCenter: string
        materialNumber: string
        assignmentNumber: string
        projectNumber: string
        establishmentCode: string
        creationDate: 2019-05-23T21:00:10Z
        creationTime: string
        exchangeRate2: 0
        withholdingType: string
        withholdingRate: 0
        withholdingDescription: string
        salesOrderDate: 2019-05-23T21:00:10Z
        salesOrderNumber: string
        purchaseOrderNumber: string
        shipperCountryVATNumber: string
        shipperCountryVATNumberUsed: string
        shipperName: string
        shipperLocalCode: string
        shipmentType: string
        shipmentDescription: string
        shipmentWeightUOM: string
        shipmentWeightGross: 0
        shipmentWeightNet: 0
        shipmentDateTime: 2019-05-23T21:00:10Z
        itemCodeType: string
        itemCode: string
        transactionEndDate: 2019-05-23T21:00:10Z
        paymentExpireDate: 2019-05-23T21:00:10Z
        paymentBankName: string
        paymentCode: string
        intBankAccountNumber: string
        originalInvoiceDate: 2019-05-23T21:00:10Z
        shipmentNumofPackages: 0
        paymentDueDate: 0
        vatDueDate: string
        virtualStamp: string
        stampAmount: 0
        reaOffice: string
        reaNumber: string
        socialCapital: 0
        soleShareholder: string
        statusLiquidation: string
        referenceProvision: string
        doacupCode: string
        doacigCode: string
        dtCtrDocumentID: string
        dtCtrDate: 2019-05-23T21:00:10Z
        dtCtrItemNum: string
        dtCtrConvCode: string
        dtCtrCUPCode: string
        dtCtrCIGCode: string
        dtCnvDocumentID: string
        dtCnvDate: 2019-05-23T21:00:10Z
        dtCnvItemNum: string
        dtCnvConvCode: string
        dtCnvCUPCode: string
        dtCnvCIGCode: string
        dtRczDocumentID: string
        dtRczDate: 2019-05-23T21:00:10Z
        dtRczItemNum: string
        dtRczConvCode: string
        dtRczCUPCode: string
        dtRczCIGCode: string
        adGestionaliType: string
        adGestionaliText: string
        adGestionaliNumber: 0
        adGestionaliDate: 2019-05-23T21:00:10Z
        adGestionaliType2: string
        adGestionaliText2: string
        adGestionaliType3: string
        adGestionaliText3: string
        adGestionaliType4: string
        adGestionaliText4: string
        adGestionaliType5: string
        adGestionaliText5: string
        lineNature: string
        lineAdminReference: string
        shipmentCause: string
        shipTimeStamp: 2019-05-23T21:00:10Z
        shipmentStartDate: 2019-05-23T21:00:10Z
        alboProfessional: string
        alboProvince: string
        alboInscriptionDate: 2019-05-23T21:00:10Z
        supplierLocalOfficeAddress: string
        supplierLocalOfficeStreetNumber: string
        supplierLocalOfficePostalCode: 0
        supplierLocalOfficeCity: string
        supplierLocalOfficeProvince: string
        supplierLocalOfficeCountry: string
        supplierFiscalRepName: string
        supplierFiscalRepTIN: string
        supplierFiscalRepFirstName: string
        supplierFiscalRepLastName: string
        supplierFiscalRepCodEORI: string
        customerLocalOfficeAddress: string
        customerLocalOfficeStreetNumber: string
        customerLocalOfficePostalCode: 0
        customerLocalOfficeCity: string
        customerLocalOfficeProvince: string
        customerLocalOfficeCountry: string
        customerFiscalRepFirstName: string
        customerFiscalRepLastName: string
        roundingAmount: 0
        socSecType: string
        socSecRate: 0
        socSecContributionAmount: 0
        socSecTaxableAmount: 0
        socSecVATRate: 0
        socSecWithheld: string
        socSecNatura: string
        socSecAdminReference: string
        art73: string
        stageReference: 0
        shipperTIN: string
        driverFirstName: string
        driverLastName: string
        resaType: string
        mainInvoiceNumber: string
        mainInvoiceDate: 2019-05-23T21:00:10Z
        subjectWithheld: string
        additionalExpenses: 0
        paymentRoundingAmount: 0
        vehicleRegistrationDate: 2019-05-23T21:00:10Z
        vehicleTotalTravel: string
        paymentBeneficiary: string
        officePostalCode: string
        signerLastName: string
        signerFirstName: string
        signerTIN: string
        abiCode: 0
        cabCode: 0
        prepaymentDiscount: 0
        prepaymentDueDate: 2019-05-23T21:00:10Z
        penaltyLatePayment: 0
        penaltyStartDate: 2019-05-23T21:00:10Z
        supplierFiscalRepTitle: string
        driverTitle: string
        doaNumItem: string
        supplierFiscalRepCountryVATNumber: string
        customerFiscalRepCountryVATNumber: string
        salesOrderNumber2: string
        salesOrderNumber3: string
        salesOrderNumber4: string
        salesOrderNumber5: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ApiTransactionRequest>
  <importProfileName>string</importProfileName>
  <fileName>string</fileName>
  <customValues>
    <property1>string</property1>
    <property2>string</property2>
  </customValues>
  <transactions>
    <companyCode>string</companyCode>
    <invoiceNumber>string</invoiceNumber>
    <salesOrderNumber>string</salesOrderNumber>
    <purchaseOrderNumber>string</purchaseOrderNumber>
    <originalInvoiceNumber>string</originalInvoiceNumber>
    <currentApprovalStatus>string</currentApprovalStatus>
    <documentType>string</documentType>
    <sequencialNumberSalesBook>string</sequencialNumberSalesBook>
    <sequencialNumberPurchaseBook>string</sequencialNumberPurchaseBook>
    <transactionDate>2019-05-23T21:00:10Z</transactionDate>
    <intrastatDate>2019-05-23T21:00:10Z</intrastatDate>
    <invoiceDate>2019-05-23T21:00:10Z</invoiceDate>
    <paymentDate>2019-05-23T21:00:10Z</paymentDate>
    <reportDate>2019-05-23T21:00:10Z</reportDate>
    <invoiceType>string</invoiceType>
    <invoiceCorrectionType>string</invoiceCorrectionType>
    <invoiceSelfBilled>true</invoiceSelfBilled>
    <taxRegimeSales>string</taxRegimeSales>
    <taxRegimePurchases>string</taxRegimePurchases>
    <customsNumber>string</customsNumber>
    <customsDate>2019-05-23T21:00:10Z</customsDate>
    <paymentMethod>string</paymentMethod>
    <bankAccount>string</bankAccount>
    <transactionCode>string</transactionCode>
    <customsValue>string</customsValue>
    <erpDocument>string</erpDocument>
    <referenceId>string</referenceId>
    <creditIndicator>string</creditIndicator>
    <lastInvoiceNumber>string</lastInvoiceNumber>
    <transactionIsDeleted>true</transactionIsDeleted>
    <accountingDocumentNumber>string</accountingDocumentNumber>
    <glDescription>string</glDescription>
    <glPostingDate>2019-05-23T21:00:10Z</glPostingDate>
    <fiscalYear>string</fiscalYear>
    <fiscalPeriod>string</fiscalPeriod>
    <erpFiscalPeriod>string</erpFiscalPeriod>
    <erpFiscalYear>string</erpFiscalYear>
    <establishmentCode>string</establishmentCode>
    <environmentCode>string</environmentCode>
    <nFeNumber>string</nFeNumber>
    <nfNumber>string</nfNumber>
    <nFeServiceNumber>string</nFeServiceNumber>
    <nFeServiceIndicator>string</nFeServiceIndicator>
    <totalValue>0</totalValue>
    <totalValue2>0</totalValue2>
    <seriesNumber>string</seriesNumber>
    <issuerID>string</issuerID>
    <partialDeduct>0</partialDeduct>
    <typeOfService>string</typeOfService>
    <withholdingSubContractor>0</withholdingSubContractor>
    <withholdingExemption>0</withholdingExemption>
    <services15>0</services15>
    <services20>0</services20>
    <services25>0</services25>
    <additionalWithholdingExemption>0</additionalWithholdingExemption>
    <cprbIndicator>string</cprbIndicator>
    <customerIdType>string</customerIdType>
    <creationDate>2019-05-23T21:00:10Z</creationDate>
    <creationTime>string</creationTime>
    <reversalOperation>0</reversalOperation>
    <reversalFiscalYear>0</reversalFiscalYear>
    <reversalCompanyCode>string</reversalCompanyCode>
    <reversalAccountingDocument>string</reversalAccountingDocument>
    <externalReference>string</externalReference>
    <originalLineNumberReference>string</originalLineNumberReference>
    <registrationNumber>string</registrationNumber>
    <paymentConditions>string</paymentConditions>
    <supplierFiscalRepName>string</supplierFiscalRepName>
    <supplierFiscalRepAddress>string</supplierFiscalRepAddress>
    <supplierFiscalDescription>string</supplierFiscalDescription>
    <customerFiscalRepName>string</customerFiscalRepName>
    <customerFiscalRepAddress>string</customerFiscalRepAddress>
    <customerFiscalDescription>string</customerFiscalDescription>
    <supplierCertifiedEmail>string</supplierCertifiedEmail>
    <customerCertifiedEmail>string</customerCertifiedEmail>
    <supplierTIN>string</supplierTIN>
    <customerTIN>string</customerTIN>
    <supplierEORICode>string</supplierEORICode>
    <customerEORICode>string</customerEORICode>
    <supplierBIC>string</supplierBIC>
    <customer>
      <businessEntityID>string</businessEntityID>
      <name>string</name>
      <billToCountry>string</billToCountry>
      <vatNumberUsed>string</vatNumberUsed>
      <countryVatNumberUsed>string</countryVatNumberUsed>
      <billToStreet>string</billToStreet>
      <billToBuildingNumber>string</billToBuildingNumber>
      <billToCity>string</billToCity>
      <billToPostalCode>string</billToPostalCode>
      <ucr>string</ucr>
      <website>string</website>
      <billToAddressDetail>string</billToAddressDetail>
      <billToRegion>string</billToRegion>
      <billToStreetNumber>string</billToStreetNumber>
      <contactFirstName>string</contactFirstName>
      <contactLastName>string</contactLastName>
      <contactTitle>string</contactTitle>
      <contactVATNumber>string</contactVATNumber>
      <deliveryDate>2019-05-23T21:00:10Z</deliveryDate>
      <deliveryId>string</deliveryId>
      <emailAddress>string</emailAddress>
      <faxNumber>string</faxNumber>
      <shipFromAddressDetail>string</shipFromAddressDetail>
      <shipFromBuildingNumber>string</shipFromBuildingNumber>
      <shipFromCity>string</shipFromCity>
      <shipFromCountry>string</shipFromCountry>
      <shipFromLocationId>string</shipFromLocationId>
      <shipFromPostalCode>string</shipFromPostalCode>
      <shipFromRegion>string</shipFromRegion>
      <shipFromStreet>string</shipFromStreet>
      <shipFromStreetNumber>string</shipFromStreetNumber>
      <shipFromWarehouseId>string</shipFromWarehouseId>
      <shipToAddressDetail>string</shipToAddressDetail>
      <shipToBuildingNumber>string</shipToBuildingNumber>
      <shipToCity>string</shipToCity>
      <shipToCountry>string</shipToCountry>
      <shipToLocationId>string</shipToLocationId>
      <shipToPostalCode>string</shipToPostalCode>
      <shipToRegion>string</shipToRegion>
      <shipToStreet>string</shipToStreet>
      <shipToStreetNumber>string</shipToStreetNumber>
      <shipToWarehouseId>string</shipToWarehouseId>
      <telephoneNumber>string</telephoneNumber>
      <fiscalRepVATNumber>string</fiscalRepVATNumber>
      <idType>string</idType>
      <idNumber>string</idNumber>
      <localTaxNumber>string</localTaxNumber>
    </customer>
    <supplier>
      <invoiceNumber>string</invoiceNumber>
      <invoiceLineNumber>string</invoiceLineNumber>
      <originalInvoiceNumber>string</originalInvoiceNumber>
      <communicationType>string</communicationType>
      <businessEntityID>string</businessEntityID>
      <name>string</name>
      <billToCountry>string</billToCountry>
      <vatNumberUsed>string</vatNumberUsed>
      <countryVatNumberUsed>string</countryVatNumberUsed>
      <billToStreet>string</billToStreet>
      <billToBuildingNumber>string</billToBuildingNumber>
      <billToCity>string</billToCity>
      <billToPostalCode>string</billToPostalCode>
      <ucr>string</ucr>
      <website>string</website>
      <billToAddressDetail>string</billToAddressDetail>
      <billToRegion>string</billToRegion>
      <billToStreetNumber>string</billToStreetNumber>
      <contactFirstName>string</contactFirstName>
      <contactLastName>string</contactLastName>
      <contactTitle>string</contactTitle>
      <contactVATNumber>string</contactVATNumber>
      <deliveryDate>2019-05-23T21:00:10Z</deliveryDate>
      <deliveryId>string</deliveryId>
      <emailAddress>string</emailAddress>
      <faxNumber>string</faxNumber>
      <shipFromAddressDetail>string</shipFromAddressDetail>
      <shipFromBuildingNumber>string</shipFromBuildingNumber>
      <shipFromCity>string</shipFromCity>
      <shipFromCountry>string</shipFromCountry>
      <shipFromLocationId>string</shipFromLocationId>
      <shipFromPostalCode>string</shipFromPostalCode>
      <shipFromRegion>string</shipFromRegion>
      <shipFromStreet>string</shipFromStreet>
      <shipFromStreetNumber>string</shipFromStreetNumber>
      <shipFromWarehouseId>string</shipFromWarehouseId>
      <shipToAddressDetail>string</shipToAddressDetail>
      <shipToBuildingNumber>string</shipToBuildingNumber>
      <shipToCity>string</shipToCity>
      <shipToCountry>string</shipToCountry>
      <shipToLocationId>string</shipToLocationId>
      <shipToPostalCode>string</shipToPostalCode>
      <shipToRegion>string</shipToRegion>
      <shipToStreet>string</shipToStreet>
      <shipToStreetNumber>string</shipToStreetNumber>
      <shipToWarehouseId>string</shipToWarehouseId>
      <telephoneNumber>string</telephoneNumber>
      <fiscalRepVATNumber>string</fiscalRepVATNumber>
      <idType>string</idType>
      <idNumber>string</idNumber>
      <localTaxNumber>string</localTaxNumber>
    </supplier>
    <lines>
      <currency>string</currency>
      <currency2>string</currency2>
      <exchangeRate>0</exchangeRate>
      <vatCode>string</vatCode>
      <vatRate>string</vatRate>
      <itemDescription>string</itemDescription>
      <itemClassification>string</itemClassification>
      <taxableBasisCredit>0</taxableBasisCredit>
      <taxableBasisDebet>0</taxableBasisDebet>
      <valueVatCredit>0</valueVatCredit>
      <valueVatDebet>0</valueVatDebet>
      <totalValueLine>0</totalValueLine>
      <amountVatDeducted>0</amountVatDeducted>
      <taxableBasisCurrency2>0</taxableBasisCurrency2>
      <valueVatCurrency2>0</valueVatCurrency2>
      <totalValueLineCurrency2>0</totalValueLineCurrency2>
      <countryDispatch>string</countryDispatch>
      <countryArrival>string</countryArrival>
      <deliveryConditions>string</deliveryConditions>
      <additionalDocumentReference>string</additionalDocumentReference>
      <reportingType>string</reportingType>
      <transactionType>0</transactionType>
      <additionalTransactionType>0</additionalTransactionType>
      <intrastatCode>string</intrastatCode>
      <extrastatCode>string</extrastatCode>
      <additionalDescription>string</additionalDescription>
      <weight>0</weight>
      <unitOfMeasure>string</unitOfMeasure>
      <quantity>0</quantity>
      <additionalUnitOfMeasure>string</additionalUnitOfMeasure>
      <commercialValue>0</commercialValue>
      <statisticalValue>0</statisticalValue>
      <commercialValueCurrency2>0</commercialValueCurrency2>
      <statisticalValueCurrency2>0</statisticalValueCurrency2>
      <itemType>string</itemType>
      <modeOfTransport>0</modeOfTransport>
      <regionDispatch>string</regionDispatch>
      <harbourDispatch>string</harbourDispatch>
      <regionArrival>string</regionArrival>
      <harbourArrival>string</harbourArrival>
      <countryOrigin>string</countryOrigin>
      <purchaseExtra1>string</purchaseExtra1>
      <purchaseExtra2>string</purchaseExtra2>
      <purchaseExtra3>string</purchaseExtra3>
      <purchaseExtra4>string</purchaseExtra4>
      <purchaseExtra5>string</purchaseExtra5>
      <purchaseExtra6>string</purchaseExtra6>
      <purchaseExtra7>string</purchaseExtra7>
      <purchaseExtra8>string</purchaseExtra8>
      <purchaseExtra9>string</purchaseExtra9>
      <purchaseExtra10>string</purchaseExtra10>
      <salesExtra1>string</salesExtra1>
      <salesExtra2>string</salesExtra2>
      <salesExtra3>string</salesExtra3>
      <salesExtra4>string</salesExtra4>
      <salesExtra5>string</salesExtra5>
      <salesExtra6>string</salesExtra6>
      <salesExtra7>string</salesExtra7>
      <salesExtra8>string</salesExtra8>
      <salesExtra9>string</salesExtra9>
      <salesExtra10>string</salesExtra10>
      <mossReporterVatNumberUsed>string</mossReporterVatNumberUsed>
      <administrationCode>string</administrationCode>
      <vatCodeAssignerCode>string</vatCodeAssignerCode>
      <isOriginal>true</isOriginal>
      <deliveryConditionsPlace>string</deliveryConditionsPlace>
      <regionOrigin>string</regionOrigin>
      <vatCodeAccountingKey>string</vatCodeAccountingKey>
      <originalTaxRateApplied>string</originalTaxRateApplied>
      <originalVatcodeUsed>string</originalVatcodeUsed>
      <originalVatcodeUsedDescription>string</originalVatcodeUsedDescription>
      <vatGlAccountCredit>string</vatGlAccountCredit>
      <vatGlAccountDebet>string</vatGlAccountDebet>
      <vatGlAccountPurchases>string</vatGlAccountPurchases>
      <vatGlAccountSales>string</vatGlAccountSales>
      <revenuesGlAccount>string</revenuesGlAccount>
      <costsGlAccount>string</costsGlAccount>
      <plantCode>string</plantCode>
      <materialTaxClassification>string</materialTaxClassification>
      <customerTaxClassification>string</customerTaxClassification>
      <invoiceLineNumber>string</invoiceLineNumber>
      <unitPrice>0</unitPrice>
      <creditNoteReason>string</creditNoteReason>
      <generalLedgerId>string</generalLedgerId>
      <generalLedgerType>string</generalLedgerType>
      <journalDescription>string</journalDescription>
      <journalId>string</journalId>
      <journalType>string</journalType>
      <statisticalProcedure>string</statisticalProcedure>
      <propertyCode>string</propertyCode>
      <propertyRegisterReference>string</propertyRegisterReference>
      <exemptReasonCode>string</exemptReasonCode>
      <utilizationDate>2019-05-23T21:00:10Z</utilizationDate>
      <annualProrate>0</annualProrate>
      <annualDeduction>0</annualDeduction>
      <annualDeductionEffectiveDate>2019-05-23T21:00:10Z</annualDeductionEffectiveDate>
      <assetId>string</assetId>
      <deliveryIdentification>string</deliveryIdentification>
      <firstSemester>true</firstSemester>
      <withholdingAmount>0</withholdingAmount>
      <operationType>string</operationType>
      <profitCenter>string</profitCenter>
      <discountBaseAmount>0</discountBaseAmount>
      <businessArea>string</businessArea>
      <costCenter>string</costCenter>
      <materialNumber>string</materialNumber>
      <assignmentNumber>string</assignmentNumber>
      <projectNumber>string</projectNumber>
      <establishmentCode>string</establishmentCode>
      <creationDate>2019-05-23T21:00:10Z</creationDate>
      <creationTime>string</creationTime>
      <exchangeRate2>0</exchangeRate2>
      <withholdingType>string</withholdingType>
      <withholdingRate>0</withholdingRate>
      <withholdingDescription>string</withholdingDescription>
      <salesOrderDate>2019-05-23T21:00:10Z</salesOrderDate>
      <salesOrderNumber>string</salesOrderNumber>
      <purchaseOrderNumber>string</purchaseOrderNumber>
      <shipperCountryVATNumber>string</shipperCountryVATNumber>
      <shipperCountryVATNumberUsed>string</shipperCountryVATNumberUsed>
      <shipperName>string</shipperName>
      <shipperLocalCode>string</shipperLocalCode>
      <shipmentType>string</shipmentType>
      <shipmentDescription>string</shipmentDescription>
      <shipmentWeightUOM>string</shipmentWeightUOM>
      <shipmentWeightGross>0</shipmentWeightGross>
      <shipmentWeightNet>0</shipmentWeightNet>
      <shipmentDateTime>2019-05-23T21:00:10Z</shipmentDateTime>
      <itemCodeType>string</itemCodeType>
      <itemCode>string</itemCode>
      <transactionEndDate>2019-05-23T21:00:10Z</transactionEndDate>
      <paymentExpireDate>2019-05-23T21:00:10Z</paymentExpireDate>
      <paymentBankName>string</paymentBankName>
      <paymentCode>string</paymentCode>
      <intBankAccountNumber>string</intBankAccountNumber>
      <originalInvoiceDate>2019-05-23T21:00:10Z</originalInvoiceDate>
      <shipmentNumofPackages>0</shipmentNumofPackages>
      <paymentDueDate>0</paymentDueDate>
      <vatDueDate>string</vatDueDate>
      <virtualStamp>string</virtualStamp>
      <stampAmount>0</stampAmount>
      <reaOffice>string</reaOffice>
      <reaNumber>string</reaNumber>
      <socialCapital>0</socialCapital>
      <soleShareholder>string</soleShareholder>
      <statusLiquidation>string</statusLiquidation>
      <referenceProvision>string</referenceProvision>
      <doacupCode>string</doacupCode>
      <doacigCode>string</doacigCode>
      <dtCtrDocumentID>string</dtCtrDocumentID>
      <dtCtrDate>2019-05-23T21:00:10Z</dtCtrDate>
      <dtCtrItemNum>string</dtCtrItemNum>
      <dtCtrConvCode>string</dtCtrConvCode>
      <dtCtrCUPCode>string</dtCtrCUPCode>
      <dtCtrCIGCode>string</dtCtrCIGCode>
      <dtCnvDocumentID>string</dtCnvDocumentID>
      <dtCnvDate>2019-05-23T21:00:10Z</dtCnvDate>
      <dtCnvItemNum>string</dtCnvItemNum>
      <dtCnvConvCode>string</dtCnvConvCode>
      <dtCnvCUPCode>string</dtCnvCUPCode>
      <dtCnvCIGCode>string</dtCnvCIGCode>
      <dtRczDocumentID>string</dtRczDocumentID>
      <dtRczDate>2019-05-23T21:00:10Z</dtRczDate>
      <dtRczItemNum>string</dtRczItemNum>
      <dtRczConvCode>string</dtRczConvCode>
      <dtRczCUPCode>string</dtRczCUPCode>
      <dtRczCIGCode>string</dtRczCIGCode>
      <adGestionaliType>string</adGestionaliType>
      <adGestionaliText>string</adGestionaliText>
      <adGestionaliNumber>0</adGestionaliNumber>
      <adGestionaliDate>2019-05-23T21:00:10Z</adGestionaliDate>
      <adGestionaliType2>string</adGestionaliType2>
      <adGestionaliText2>string</adGestionaliText2>
      <adGestionaliType3>string</adGestionaliType3>
      <adGestionaliText3>string</adGestionaliText3>
      <adGestionaliType4>string</adGestionaliType4>
      <adGestionaliText4>string</adGestionaliText4>
      <adGestionaliType5>string</adGestionaliType5>
      <adGestionaliText5>string</adGestionaliText5>
      <lineNature>string</lineNature>
      <lineAdminReference>string</lineAdminReference>
      <shipmentCause>string</shipmentCause>
      <shipTimeStamp>2019-05-23T21:00:10Z</shipTimeStamp>
      <shipmentStartDate>2019-05-23T21:00:10Z</shipmentStartDate>
      <alboProfessional>string</alboProfessional>
      <alboProvince>string</alboProvince>
      <alboInscriptionDate>2019-05-23T21:00:10Z</alboInscriptionDate>
      <supplierLocalOfficeAddress>string</supplierLocalOfficeAddress>
      <supplierLocalOfficeStreetNumber>string</supplierLocalOfficeStreetNumber>
      <supplierLocalOfficePostalCode>0</supplierLocalOfficePostalCode>
      <supplierLocalOfficeCity>string</supplierLocalOfficeCity>
      <supplierLocalOfficeProvince>string</supplierLocalOfficeProvince>
      <supplierLocalOfficeCountry>string</supplierLocalOfficeCountry>
      <supplierFiscalRepName>string</supplierFiscalRepName>
      <supplierFiscalRepTIN>string</supplierFiscalRepTIN>
      <supplierFiscalRepFirstName>string</supplierFiscalRepFirstName>
      <supplierFiscalRepLastName>string</supplierFiscalRepLastName>
      <supplierFiscalRepCodEORI>string</supplierFiscalRepCodEORI>
      <customerLocalOfficeAddress>string</customerLocalOfficeAddress>
      <customerLocalOfficeStreetNumber>string</customerLocalOfficeStreetNumber>
      <customerLocalOfficePostalCode>0</customerLocalOfficePostalCode>
      <customerLocalOfficeCity>string</customerLocalOfficeCity>
      <customerLocalOfficeProvince>string</customerLocalOfficeProvince>
      <customerLocalOfficeCountry>string</customerLocalOfficeCountry>
      <customerFiscalRepFirstName>string</customerFiscalRepFirstName>
      <customerFiscalRepLastName>string</customerFiscalRepLastName>
      <roundingAmount>0</roundingAmount>
      <socSecType>string</socSecType>
      <socSecRate>0</socSecRate>
      <socSecContributionAmount>0</socSecContributionAmount>
      <socSecTaxableAmount>0</socSecTaxableAmount>
      <socSecVATRate>0</socSecVATRate>
      <socSecWithheld>string</socSecWithheld>
      <socSecNatura>string</socSecNatura>
      <socSecAdminReference>string</socSecAdminReference>
      <art73>string</art73>
      <stageReference>0</stageReference>
      <shipperTIN>string</shipperTIN>
      <driverFirstName>string</driverFirstName>
      <driverLastName>string</driverLastName>
      <resaType>string</resaType>
      <mainInvoiceNumber>string</mainInvoiceNumber>
      <mainInvoiceDate>2019-05-23T21:00:10Z</mainInvoiceDate>
      <subjectWithheld>string</subjectWithheld>
      <additionalExpenses>0</additionalExpenses>
      <paymentRoundingAmount>0</paymentRoundingAmount>
      <vehicleRegistrationDate>2019-05-23T21:00:10Z</vehicleRegistrationDate>
      <vehicleTotalTravel>string</vehicleTotalTravel>
      <paymentBeneficiary>string</paymentBeneficiary>
      <officePostalCode>string</officePostalCode>
      <signerLastName>string</signerLastName>
      <signerFirstName>string</signerFirstName>
      <signerTIN>string</signerTIN>
      <abiCode>0</abiCode>
      <cabCode>0</cabCode>
      <prepaymentDiscount>0</prepaymentDiscount>
      <prepaymentDueDate>2019-05-23T21:00:10Z</prepaymentDueDate>
      <penaltyLatePayment>0</penaltyLatePayment>
      <penaltyStartDate>2019-05-23T21:00:10Z</penaltyStartDate>
      <supplierFiscalRepTitle>string</supplierFiscalRepTitle>
      <driverTitle>string</driverTitle>
      <doaNumItem>string</doaNumItem>
      <supplierFiscalRepCountryVATNumber>string</supplierFiscalRepCountryVATNumber>
      <customerFiscalRepCountryVATNumber>string</customerFiscalRepCountryVATNumber>
      <salesOrderNumber2>string</salesOrderNumber2>
      <salesOrderNumber3>string</salesOrderNumber3>
      <salesOrderNumber4>string</salesOrderNumber4>
      <salesOrderNumber5>string</salesOrderNumber5>
    </lines>
  </transactions>
</ApiTransactionRequest>
```

<section>
<h3 id="creates-transactions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ApiTransactionRequest](#schemaapitransactionrequest)|true|max of 100 transactions to create|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="creates-transactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="creates-transactions-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>
<h1 id="vatware-api-transactionsv2">TransactionsV2</h1>

<section>

## TransactionsV2_Index

<a id="opIdTransactionsV2_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://uatvat-api.sovos.com/api/v2/transactions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
DELETE https://uatvat-api.sovos.com/api/v2/transactions HTTP/1.1
Host: uatvat-api.sovos.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "companyCode": "string",
  "invoiceNumber": "string",
  "salesOrderNumber": "string",
  "purchaseOrderNumber": "string",
  "originalInvoiceNumber": "string",
  "currentApprovalStatus": "string",
  "documentType": "string",
  "sequencialNumberSalesBook": "string",
  "sequencialNumberPurchaseBook": "string",
  "transactionDate": "2019-05-23T21:00:10Z",
  "intrastatDate": "2019-05-23T21:00:10Z",
  "invoiceDate": "2019-05-23T21:00:10Z",
  "paymentDate": "2019-05-23T21:00:10Z",
  "reportDate": "2019-05-23T21:00:10Z",
  "invoiceType": "string",
  "invoiceCorrectionType": "string",
  "invoiceSelfBilled": true,
  "taxRegimeSales": "string",
  "taxRegimePurchases": "string",
  "customsNumber": "string",
  "customsDate": "2019-05-23T21:00:10Z",
  "paymentMethod": "string",
  "bankAccount": "string",
  "transactionCode": "string",
  "customsValue": "string",
  "erpDocument": "string",
  "referenceId": "string",
  "creditIndicator": "string",
  "lastInvoiceNumber": "string",
  "transactionIsDeleted": true,
  "accountingDocumentNumber": "string",
  "glDescription": "string",
  "glPostingDate": "2019-05-23T21:00:10Z",
  "fiscalYear": "string",
  "fiscalPeriod": "string",
  "erpFiscalPeriod": "string",
  "erpFiscalYear": "string",
  "establishmentCode": "string",
  "environmentCode": "string",
  "nFeNumber": "string",
  "nfNumber": "string",
  "nFeServiceNumber": "string",
  "nFeServiceIndicator": "string",
  "totalValue": 0,
  "totalValue2": 0,
  "seriesNumber": "string",
  "issuerID": "string",
  "partialDeduct": 0,
  "typeOfService": "string",
  "withholdingSubContractor": 0,
  "withholdingExemption": 0,
  "services15": 0,
  "services20": 0,
  "services25": 0,
  "additionalWithholdingExemption": 0,
  "cprbIndicator": "string",
  "customerIdType": "string",
  "creationDate": "2019-05-23T21:00:10Z",
  "creationTime": "string",
  "reversalOperation": 0,
  "reversalFiscalYear": 0,
  "reversalCompanyCode": "string",
  "reversalAccountingDocument": "string",
  "externalReference": "string",
  "originalLineNumberReference": "string",
  "registrationNumber": "string",
  "paymentConditions": "string",
  "supplierFiscalRepName": "string",
  "supplierFiscalRepAddress": "string",
  "supplierFiscalDescription": "string",
  "customerFiscalRepName": "string",
  "customerFiscalRepAddress": "string",
  "customerFiscalDescription": "string",
  "supplierCertifiedEmail": "string",
  "customerCertifiedEmail": "string",
  "supplierTIN": "string",
  "customerTIN": "string",
  "supplierEORICode": "string",
  "customerEORICode": "string",
  "supplierBIC": "string",
  "customer": {
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "supplier": {
    "invoiceNumber": "string",
    "invoiceLineNumber": "string",
    "originalInvoiceNumber": "string",
    "communicationType": "string",
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "lines": [
    {
      "currency": "string",
      "currency2": "string",
      "exchangeRate": 0,
      "vatCode": "string",
      "vatRate": "string",
      "itemDescription": "string",
      "itemClassification": "string",
      "taxableBasisCredit": 0,
      "taxableBasisDebet": 0,
      "valueVatCredit": 0,
      "valueVatDebet": 0,
      "totalValueLine": 0,
      "amountVatDeducted": 0,
      "taxableBasisCurrency2": 0,
      "valueVatCurrency2": 0,
      "totalValueLineCurrency2": 0,
      "countryDispatch": "string",
      "countryArrival": "string",
      "deliveryConditions": "string",
      "additionalDocumentReference": "string",
      "reportingType": "string",
      "transactionType": 0,
      "additionalTransactionType": 0,
      "intrastatCode": "string",
      "extrastatCode": "string",
      "additionalDescription": "string",
      "weight": 0,
      "unitOfMeasure": "string",
      "quantity": 0,
      "additionalUnitOfMeasure": "string",
      "commercialValue": 0,
      "statisticalValue": 0,
      "commercialValueCurrency2": 0,
      "statisticalValueCurrency2": 0,
      "itemType": "string",
      "modeOfTransport": 0,
      "regionDispatch": "string",
      "harbourDispatch": "string",
      "regionArrival": "string",
      "harbourArrival": "string",
      "countryOrigin": "string",
      "purchaseExtra1": "string",
      "purchaseExtra2": "string",
      "purchaseExtra3": "string",
      "purchaseExtra4": "string",
      "purchaseExtra5": "string",
      "purchaseExtra6": "string",
      "purchaseExtra7": "string",
      "purchaseExtra8": "string",
      "purchaseExtra9": "string",
      "purchaseExtra10": "string",
      "salesExtra1": "string",
      "salesExtra2": "string",
      "salesExtra3": "string",
      "salesExtra4": "string",
      "salesExtra5": "string",
      "salesExtra6": "string",
      "salesExtra7": "string",
      "salesExtra8": "string",
      "salesExtra9": "string",
      "salesExtra10": "string",
      "mossReporterVatNumberUsed": "string",
      "administrationCode": "string",
      "vatCodeAssignerCode": "string",
      "isOriginal": true,
      "deliveryConditionsPlace": "string",
      "regionOrigin": "string",
      "vatCodeAccountingKey": "string",
      "originalTaxRateApplied": "string",
      "originalVatcodeUsed": "string",
      "originalVatcodeUsedDescription": "string",
      "vatGlAccountCredit": "string",
      "vatGlAccountDebet": "string",
      "vatGlAccountPurchases": "string",
      "vatGlAccountSales": "string",
      "revenuesGlAccount": "string",
      "costsGlAccount": "string",
      "plantCode": "string",
      "materialTaxClassification": "string",
      "customerTaxClassification": "string",
      "invoiceLineNumber": "string",
      "unitPrice": 0,
      "creditNoteReason": "string",
      "generalLedgerId": "string",
      "generalLedgerType": "string",
      "journalDescription": "string",
      "journalId": "string",
      "journalType": "string",
      "statisticalProcedure": "string",
      "propertyCode": "string",
      "propertyRegisterReference": "string",
      "exemptReasonCode": "string",
      "utilizationDate": "2019-05-23T21:00:10Z",
      "annualProrate": 0,
      "annualDeduction": 0,
      "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
      "assetId": "string",
      "deliveryIdentification": "string",
      "firstSemester": true,
      "withholdingAmount": 0,
      "operationType": "string",
      "profitCenter": "string",
      "discountBaseAmount": 0,
      "businessArea": "string",
      "costCenter": "string",
      "materialNumber": "string",
      "assignmentNumber": "string",
      "projectNumber": "string",
      "establishmentCode": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "exchangeRate2": 0,
      "withholdingType": "string",
      "withholdingRate": 0,
      "withholdingDescription": "string",
      "salesOrderDate": "2019-05-23T21:00:10Z",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "shipperCountryVATNumber": "string",
      "shipperCountryVATNumberUsed": "string",
      "shipperName": "string",
      "shipperLocalCode": "string",
      "shipmentType": "string",
      "shipmentDescription": "string",
      "shipmentWeightUOM": "string",
      "shipmentWeightGross": 0,
      "shipmentWeightNet": 0,
      "shipmentDateTime": "2019-05-23T21:00:10Z",
      "itemCodeType": "string",
      "itemCode": "string",
      "transactionEndDate": "2019-05-23T21:00:10Z",
      "paymentExpireDate": "2019-05-23T21:00:10Z",
      "paymentBankName": "string",
      "paymentCode": "string",
      "intBankAccountNumber": "string",
      "originalInvoiceDate": "2019-05-23T21:00:10Z",
      "shipmentNumofPackages": 0,
      "paymentDueDate": 0,
      "vatDueDate": "string",
      "virtualStamp": "string",
      "stampAmount": 0,
      "reaOffice": "string",
      "reaNumber": "string",
      "socialCapital": 0,
      "soleShareholder": "string",
      "statusLiquidation": "string",
      "referenceProvision": "string",
      "doacupCode": "string",
      "doacigCode": "string",
      "dtCtrDocumentID": "string",
      "dtCtrDate": "2019-05-23T21:00:10Z",
      "dtCtrItemNum": "string",
      "dtCtrConvCode": "string",
      "dtCtrCUPCode": "string",
      "dtCtrCIGCode": "string",
      "dtCnvDocumentID": "string",
      "dtCnvDate": "2019-05-23T21:00:10Z",
      "dtCnvItemNum": "string",
      "dtCnvConvCode": "string",
      "dtCnvCUPCode": "string",
      "dtCnvCIGCode": "string",
      "dtRczDocumentID": "string",
      "dtRczDate": "2019-05-23T21:00:10Z",
      "dtRczItemNum": "string",
      "dtRczConvCode": "string",
      "dtRczCUPCode": "string",
      "dtRczCIGCode": "string",
      "adGestionaliType": "string",
      "adGestionaliText": "string",
      "adGestionaliNumber": 0,
      "adGestionaliDate": "2019-05-23T21:00:10Z",
      "adGestionaliType2": "string",
      "adGestionaliText2": "string",
      "adGestionaliType3": "string",
      "adGestionaliText3": "string",
      "adGestionaliType4": "string",
      "adGestionaliText4": "string",
      "adGestionaliType5": "string",
      "adGestionaliText5": "string",
      "lineNature": "string",
      "lineAdminReference": "string",
      "shipmentCause": "string",
      "shipTimeStamp": "2019-05-23T21:00:10Z",
      "shipmentStartDate": "2019-05-23T21:00:10Z",
      "alboProfessional": "string",
      "alboProvince": "string",
      "alboInscriptionDate": "2019-05-23T21:00:10Z",
      "supplierLocalOfficeAddress": "string",
      "supplierLocalOfficeStreetNumber": "string",
      "supplierLocalOfficePostalCode": 0,
      "supplierLocalOfficeCity": "string",
      "supplierLocalOfficeProvince": "string",
      "supplierLocalOfficeCountry": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepTIN": "string",
      "supplierFiscalRepFirstName": "string",
      "supplierFiscalRepLastName": "string",
      "supplierFiscalRepCodEORI": "string",
      "customerLocalOfficeAddress": "string",
      "customerLocalOfficeStreetNumber": "string",
      "customerLocalOfficePostalCode": 0,
      "customerLocalOfficeCity": "string",
      "customerLocalOfficeProvince": "string",
      "customerLocalOfficeCountry": "string",
      "customerFiscalRepFirstName": "string",
      "customerFiscalRepLastName": "string",
      "roundingAmount": 0,
      "socSecType": "string",
      "socSecRate": 0,
      "socSecContributionAmount": 0,
      "socSecTaxableAmount": 0,
      "socSecVATRate": 0,
      "socSecWithheld": "string",
      "socSecNatura": "string",
      "socSecAdminReference": "string",
      "art73": "string",
      "stageReference": 0,
      "shipperTIN": "string",
      "driverFirstName": "string",
      "driverLastName": "string",
      "resaType": "string",
      "mainInvoiceNumber": "string",
      "mainInvoiceDate": "2019-05-23T21:00:10Z",
      "subjectWithheld": "string",
      "additionalExpenses": 0,
      "paymentRoundingAmount": 0,
      "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
      "vehicleTotalTravel": "string",
      "paymentBeneficiary": "string",
      "officePostalCode": "string",
      "signerLastName": "string",
      "signerFirstName": "string",
      "signerTIN": "string",
      "abiCode": 0,
      "cabCode": 0,
      "prepaymentDiscount": 0,
      "prepaymentDueDate": "2019-05-23T21:00:10Z",
      "penaltyLatePayment": 0,
      "penaltyStartDate": "2019-05-23T21:00:10Z",
      "supplierFiscalRepTitle": "string",
      "driverTitle": "string",
      "doaNumItem": "string",
      "supplierFiscalRepCountryVATNumber": "string",
      "customerFiscalRepCountryVATNumber": "string",
      "salesOrderNumber2": "string",
      "salesOrderNumber3": "string",
      "salesOrderNumber4": "string",
      "salesOrderNumber5": "string"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/v2/transactions',
{
  method: 'DELETE',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.delete 'https://uatvat-api.sovos.com/api/v2/transactions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.delete('https://uatvat-api.sovos.com/api/v2/transactions', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://uatvat-api.sovos.com/api/v2/transactions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/v2/transactions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://uatvat-api.sovos.com/api/v2/transactions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/transactions`

> Body parameter

```json
{
  "companyCode": "string",
  "invoiceNumber": "string",
  "salesOrderNumber": "string",
  "purchaseOrderNumber": "string",
  "originalInvoiceNumber": "string",
  "currentApprovalStatus": "string",
  "documentType": "string",
  "sequencialNumberSalesBook": "string",
  "sequencialNumberPurchaseBook": "string",
  "transactionDate": "2019-05-23T21:00:10Z",
  "intrastatDate": "2019-05-23T21:00:10Z",
  "invoiceDate": "2019-05-23T21:00:10Z",
  "paymentDate": "2019-05-23T21:00:10Z",
  "reportDate": "2019-05-23T21:00:10Z",
  "invoiceType": "string",
  "invoiceCorrectionType": "string",
  "invoiceSelfBilled": true,
  "taxRegimeSales": "string",
  "taxRegimePurchases": "string",
  "customsNumber": "string",
  "customsDate": "2019-05-23T21:00:10Z",
  "paymentMethod": "string",
  "bankAccount": "string",
  "transactionCode": "string",
  "customsValue": "string",
  "erpDocument": "string",
  "referenceId": "string",
  "creditIndicator": "string",
  "lastInvoiceNumber": "string",
  "transactionIsDeleted": true,
  "accountingDocumentNumber": "string",
  "glDescription": "string",
  "glPostingDate": "2019-05-23T21:00:10Z",
  "fiscalYear": "string",
  "fiscalPeriod": "string",
  "erpFiscalPeriod": "string",
  "erpFiscalYear": "string",
  "establishmentCode": "string",
  "environmentCode": "string",
  "nFeNumber": "string",
  "nfNumber": "string",
  "nFeServiceNumber": "string",
  "nFeServiceIndicator": "string",
  "totalValue": 0,
  "totalValue2": 0,
  "seriesNumber": "string",
  "issuerID": "string",
  "partialDeduct": 0,
  "typeOfService": "string",
  "withholdingSubContractor": 0,
  "withholdingExemption": 0,
  "services15": 0,
  "services20": 0,
  "services25": 0,
  "additionalWithholdingExemption": 0,
  "cprbIndicator": "string",
  "customerIdType": "string",
  "creationDate": "2019-05-23T21:00:10Z",
  "creationTime": "string",
  "reversalOperation": 0,
  "reversalFiscalYear": 0,
  "reversalCompanyCode": "string",
  "reversalAccountingDocument": "string",
  "externalReference": "string",
  "originalLineNumberReference": "string",
  "registrationNumber": "string",
  "paymentConditions": "string",
  "supplierFiscalRepName": "string",
  "supplierFiscalRepAddress": "string",
  "supplierFiscalDescription": "string",
  "customerFiscalRepName": "string",
  "customerFiscalRepAddress": "string",
  "customerFiscalDescription": "string",
  "supplierCertifiedEmail": "string",
  "customerCertifiedEmail": "string",
  "supplierTIN": "string",
  "customerTIN": "string",
  "supplierEORICode": "string",
  "customerEORICode": "string",
  "supplierBIC": "string",
  "customer": {
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "supplier": {
    "invoiceNumber": "string",
    "invoiceLineNumber": "string",
    "originalInvoiceNumber": "string",
    "communicationType": "string",
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "lines": [
    {
      "currency": "string",
      "currency2": "string",
      "exchangeRate": 0,
      "vatCode": "string",
      "vatRate": "string",
      "itemDescription": "string",
      "itemClassification": "string",
      "taxableBasisCredit": 0,
      "taxableBasisDebet": 0,
      "valueVatCredit": 0,
      "valueVatDebet": 0,
      "totalValueLine": 0,
      "amountVatDeducted": 0,
      "taxableBasisCurrency2": 0,
      "valueVatCurrency2": 0,
      "totalValueLineCurrency2": 0,
      "countryDispatch": "string",
      "countryArrival": "string",
      "deliveryConditions": "string",
      "additionalDocumentReference": "string",
      "reportingType": "string",
      "transactionType": 0,
      "additionalTransactionType": 0,
      "intrastatCode": "string",
      "extrastatCode": "string",
      "additionalDescription": "string",
      "weight": 0,
      "unitOfMeasure": "string",
      "quantity": 0,
      "additionalUnitOfMeasure": "string",
      "commercialValue": 0,
      "statisticalValue": 0,
      "commercialValueCurrency2": 0,
      "statisticalValueCurrency2": 0,
      "itemType": "string",
      "modeOfTransport": 0,
      "regionDispatch": "string",
      "harbourDispatch": "string",
      "regionArrival": "string",
      "harbourArrival": "string",
      "countryOrigin": "string",
      "purchaseExtra1": "string",
      "purchaseExtra2": "string",
      "purchaseExtra3": "string",
      "purchaseExtra4": "string",
      "purchaseExtra5": "string",
      "purchaseExtra6": "string",
      "purchaseExtra7": "string",
      "purchaseExtra8": "string",
      "purchaseExtra9": "string",
      "purchaseExtra10": "string",
      "salesExtra1": "string",
      "salesExtra2": "string",
      "salesExtra3": "string",
      "salesExtra4": "string",
      "salesExtra5": "string",
      "salesExtra6": "string",
      "salesExtra7": "string",
      "salesExtra8": "string",
      "salesExtra9": "string",
      "salesExtra10": "string",
      "mossReporterVatNumberUsed": "string",
      "administrationCode": "string",
      "vatCodeAssignerCode": "string",
      "isOriginal": true,
      "deliveryConditionsPlace": "string",
      "regionOrigin": "string",
      "vatCodeAccountingKey": "string",
      "originalTaxRateApplied": "string",
      "originalVatcodeUsed": "string",
      "originalVatcodeUsedDescription": "string",
      "vatGlAccountCredit": "string",
      "vatGlAccountDebet": "string",
      "vatGlAccountPurchases": "string",
      "vatGlAccountSales": "string",
      "revenuesGlAccount": "string",
      "costsGlAccount": "string",
      "plantCode": "string",
      "materialTaxClassification": "string",
      "customerTaxClassification": "string",
      "invoiceLineNumber": "string",
      "unitPrice": 0,
      "creditNoteReason": "string",
      "generalLedgerId": "string",
      "generalLedgerType": "string",
      "journalDescription": "string",
      "journalId": "string",
      "journalType": "string",
      "statisticalProcedure": "string",
      "propertyCode": "string",
      "propertyRegisterReference": "string",
      "exemptReasonCode": "string",
      "utilizationDate": "2019-05-23T21:00:10Z",
      "annualProrate": 0,
      "annualDeduction": 0,
      "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
      "assetId": "string",
      "deliveryIdentification": "string",
      "firstSemester": true,
      "withholdingAmount": 0,
      "operationType": "string",
      "profitCenter": "string",
      "discountBaseAmount": 0,
      "businessArea": "string",
      "costCenter": "string",
      "materialNumber": "string",
      "assignmentNumber": "string",
      "projectNumber": "string",
      "establishmentCode": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "exchangeRate2": 0,
      "withholdingType": "string",
      "withholdingRate": 0,
      "withholdingDescription": "string",
      "salesOrderDate": "2019-05-23T21:00:10Z",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "shipperCountryVATNumber": "string",
      "shipperCountryVATNumberUsed": "string",
      "shipperName": "string",
      "shipperLocalCode": "string",
      "shipmentType": "string",
      "shipmentDescription": "string",
      "shipmentWeightUOM": "string",
      "shipmentWeightGross": 0,
      "shipmentWeightNet": 0,
      "shipmentDateTime": "2019-05-23T21:00:10Z",
      "itemCodeType": "string",
      "itemCode": "string",
      "transactionEndDate": "2019-05-23T21:00:10Z",
      "paymentExpireDate": "2019-05-23T21:00:10Z",
      "paymentBankName": "string",
      "paymentCode": "string",
      "intBankAccountNumber": "string",
      "originalInvoiceDate": "2019-05-23T21:00:10Z",
      "shipmentNumofPackages": 0,
      "paymentDueDate": 0,
      "vatDueDate": "string",
      "virtualStamp": "string",
      "stampAmount": 0,
      "reaOffice": "string",
      "reaNumber": "string",
      "socialCapital": 0,
      "soleShareholder": "string",
      "statusLiquidation": "string",
      "referenceProvision": "string",
      "doacupCode": "string",
      "doacigCode": "string",
      "dtCtrDocumentID": "string",
      "dtCtrDate": "2019-05-23T21:00:10Z",
      "dtCtrItemNum": "string",
      "dtCtrConvCode": "string",
      "dtCtrCUPCode": "string",
      "dtCtrCIGCode": "string",
      "dtCnvDocumentID": "string",
      "dtCnvDate": "2019-05-23T21:00:10Z",
      "dtCnvItemNum": "string",
      "dtCnvConvCode": "string",
      "dtCnvCUPCode": "string",
      "dtCnvCIGCode": "string",
      "dtRczDocumentID": "string",
      "dtRczDate": "2019-05-23T21:00:10Z",
      "dtRczItemNum": "string",
      "dtRczConvCode": "string",
      "dtRczCUPCode": "string",
      "dtRczCIGCode": "string",
      "adGestionaliType": "string",
      "adGestionaliText": "string",
      "adGestionaliNumber": 0,
      "adGestionaliDate": "2019-05-23T21:00:10Z",
      "adGestionaliType2": "string",
      "adGestionaliText2": "string",
      "adGestionaliType3": "string",
      "adGestionaliText3": "string",
      "adGestionaliType4": "string",
      "adGestionaliText4": "string",
      "adGestionaliType5": "string",
      "adGestionaliText5": "string",
      "lineNature": "string",
      "lineAdminReference": "string",
      "shipmentCause": "string",
      "shipTimeStamp": "2019-05-23T21:00:10Z",
      "shipmentStartDate": "2019-05-23T21:00:10Z",
      "alboProfessional": "string",
      "alboProvince": "string",
      "alboInscriptionDate": "2019-05-23T21:00:10Z",
      "supplierLocalOfficeAddress": "string",
      "supplierLocalOfficeStreetNumber": "string",
      "supplierLocalOfficePostalCode": 0,
      "supplierLocalOfficeCity": "string",
      "supplierLocalOfficeProvince": "string",
      "supplierLocalOfficeCountry": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepTIN": "string",
      "supplierFiscalRepFirstName": "string",
      "supplierFiscalRepLastName": "string",
      "supplierFiscalRepCodEORI": "string",
      "customerLocalOfficeAddress": "string",
      "customerLocalOfficeStreetNumber": "string",
      "customerLocalOfficePostalCode": 0,
      "customerLocalOfficeCity": "string",
      "customerLocalOfficeProvince": "string",
      "customerLocalOfficeCountry": "string",
      "customerFiscalRepFirstName": "string",
      "customerFiscalRepLastName": "string",
      "roundingAmount": 0,
      "socSecType": "string",
      "socSecRate": 0,
      "socSecContributionAmount": 0,
      "socSecTaxableAmount": 0,
      "socSecVATRate": 0,
      "socSecWithheld": "string",
      "socSecNatura": "string",
      "socSecAdminReference": "string",
      "art73": "string",
      "stageReference": 0,
      "shipperTIN": "string",
      "driverFirstName": "string",
      "driverLastName": "string",
      "resaType": "string",
      "mainInvoiceNumber": "string",
      "mainInvoiceDate": "2019-05-23T21:00:10Z",
      "subjectWithheld": "string",
      "additionalExpenses": 0,
      "paymentRoundingAmount": 0,
      "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
      "vehicleTotalTravel": "string",
      "paymentBeneficiary": "string",
      "officePostalCode": "string",
      "signerLastName": "string",
      "signerFirstName": "string",
      "signerTIN": "string",
      "abiCode": 0,
      "cabCode": 0,
      "prepaymentDiscount": 0,
      "prepaymentDueDate": "2019-05-23T21:00:10Z",
      "penaltyLatePayment": 0,
      "penaltyStartDate": "2019-05-23T21:00:10Z",
      "supplierFiscalRepTitle": "string",
      "driverTitle": "string",
      "doaNumItem": "string",
      "supplierFiscalRepCountryVATNumber": "string",
      "customerFiscalRepCountryVATNumber": "string",
      "salesOrderNumber2": "string",
      "salesOrderNumber3": "string",
      "salesOrderNumber4": "string",
      "salesOrderNumber5": "string"
    }
  ]
}
```

```yaml
companyCode: string
invoiceNumber: string
salesOrderNumber: string
purchaseOrderNumber: string
originalInvoiceNumber: string
currentApprovalStatus: string
documentType: string
sequencialNumberSalesBook: string
sequencialNumberPurchaseBook: string
transactionDate: 2019-05-23T21:00:10Z
intrastatDate: 2019-05-23T21:00:10Z
invoiceDate: 2019-05-23T21:00:10Z
paymentDate: 2019-05-23T21:00:10Z
reportDate: 2019-05-23T21:00:10Z
invoiceType: string
invoiceCorrectionType: string
invoiceSelfBilled: true
taxRegimeSales: string
taxRegimePurchases: string
customsNumber: string
customsDate: 2019-05-23T21:00:10Z
paymentMethod: string
bankAccount: string
transactionCode: string
customsValue: string
erpDocument: string
referenceId: string
creditIndicator: string
lastInvoiceNumber: string
transactionIsDeleted: true
accountingDocumentNumber: string
glDescription: string
glPostingDate: 2019-05-23T21:00:10Z
fiscalYear: string
fiscalPeriod: string
erpFiscalPeriod: string
erpFiscalYear: string
establishmentCode: string
environmentCode: string
nFeNumber: string
nfNumber: string
nFeServiceNumber: string
nFeServiceIndicator: string
totalValue: 0
totalValue2: 0
seriesNumber: string
issuerID: string
partialDeduct: 0
typeOfService: string
withholdingSubContractor: 0
withholdingExemption: 0
services15: 0
services20: 0
services25: 0
additionalWithholdingExemption: 0
cprbIndicator: string
customerIdType: string
creationDate: 2019-05-23T21:00:10Z
creationTime: string
reversalOperation: 0
reversalFiscalYear: 0
reversalCompanyCode: string
reversalAccountingDocument: string
externalReference: string
originalLineNumberReference: string
registrationNumber: string
paymentConditions: string
supplierFiscalRepName: string
supplierFiscalRepAddress: string
supplierFiscalDescription: string
customerFiscalRepName: string
customerFiscalRepAddress: string
customerFiscalDescription: string
supplierCertifiedEmail: string
customerCertifiedEmail: string
supplierTIN: string
customerTIN: string
supplierEORICode: string
customerEORICode: string
supplierBIC: string
customer:
  businessEntityID: string
  name: string
  billToCountry: string
  vatNumberUsed: string
  countryVatNumberUsed: string
  billToStreet: string
  billToBuildingNumber: string
  billToCity: string
  billToPostalCode: string
  ucr: string
  website: string
  billToAddressDetail: string
  billToRegion: string
  billToStreetNumber: string
  contactFirstName: string
  contactLastName: string
  contactTitle: string
  contactVATNumber: string
  deliveryDate: 2019-05-23T21:00:10Z
  deliveryId: string
  emailAddress: string
  faxNumber: string
  shipFromAddressDetail: string
  shipFromBuildingNumber: string
  shipFromCity: string
  shipFromCountry: string
  shipFromLocationId: string
  shipFromPostalCode: string
  shipFromRegion: string
  shipFromStreet: string
  shipFromStreetNumber: string
  shipFromWarehouseId: string
  shipToAddressDetail: string
  shipToBuildingNumber: string
  shipToCity: string
  shipToCountry: string
  shipToLocationId: string
  shipToPostalCode: string
  shipToRegion: string
  shipToStreet: string
  shipToStreetNumber: string
  shipToWarehouseId: string
  telephoneNumber: string
  fiscalRepVATNumber: string
  idType: string
  idNumber: string
  localTaxNumber: string
supplier:
  invoiceNumber: string
  invoiceLineNumber: string
  originalInvoiceNumber: string
  communicationType: string
  businessEntityID: string
  name: string
  billToCountry: string
  vatNumberUsed: string
  countryVatNumberUsed: string
  billToStreet: string
  billToBuildingNumber: string
  billToCity: string
  billToPostalCode: string
  ucr: string
  website: string
  billToAddressDetail: string
  billToRegion: string
  billToStreetNumber: string
  contactFirstName: string
  contactLastName: string
  contactTitle: string
  contactVATNumber: string
  deliveryDate: 2019-05-23T21:00:10Z
  deliveryId: string
  emailAddress: string
  faxNumber: string
  shipFromAddressDetail: string
  shipFromBuildingNumber: string
  shipFromCity: string
  shipFromCountry: string
  shipFromLocationId: string
  shipFromPostalCode: string
  shipFromRegion: string
  shipFromStreet: string
  shipFromStreetNumber: string
  shipFromWarehouseId: string
  shipToAddressDetail: string
  shipToBuildingNumber: string
  shipToCity: string
  shipToCountry: string
  shipToLocationId: string
  shipToPostalCode: string
  shipToRegion: string
  shipToStreet: string
  shipToStreetNumber: string
  shipToWarehouseId: string
  telephoneNumber: string
  fiscalRepVATNumber: string
  idType: string
  idNumber: string
  localTaxNumber: string
lines:
  - currency: string
    currency2: string
    exchangeRate: 0
    vatCode: string
    vatRate: string
    itemDescription: string
    itemClassification: string
    taxableBasisCredit: 0
    taxableBasisDebet: 0
    valueVatCredit: 0
    valueVatDebet: 0
    totalValueLine: 0
    amountVatDeducted: 0
    taxableBasisCurrency2: 0
    valueVatCurrency2: 0
    totalValueLineCurrency2: 0
    countryDispatch: string
    countryArrival: string
    deliveryConditions: string
    additionalDocumentReference: string
    reportingType: string
    transactionType: 0
    additionalTransactionType: 0
    intrastatCode: string
    extrastatCode: string
    additionalDescription: string
    weight: 0
    unitOfMeasure: string
    quantity: 0
    additionalUnitOfMeasure: string
    commercialValue: 0
    statisticalValue: 0
    commercialValueCurrency2: 0
    statisticalValueCurrency2: 0
    itemType: string
    modeOfTransport: 0
    regionDispatch: string
    harbourDispatch: string
    regionArrival: string
    harbourArrival: string
    countryOrigin: string
    purchaseExtra1: string
    purchaseExtra2: string
    purchaseExtra3: string
    purchaseExtra4: string
    purchaseExtra5: string
    purchaseExtra6: string
    purchaseExtra7: string
    purchaseExtra8: string
    purchaseExtra9: string
    purchaseExtra10: string
    salesExtra1: string
    salesExtra2: string
    salesExtra3: string
    salesExtra4: string
    salesExtra5: string
    salesExtra6: string
    salesExtra7: string
    salesExtra8: string
    salesExtra9: string
    salesExtra10: string
    mossReporterVatNumberUsed: string
    administrationCode: string
    vatCodeAssignerCode: string
    isOriginal: true
    deliveryConditionsPlace: string
    regionOrigin: string
    vatCodeAccountingKey: string
    originalTaxRateApplied: string
    originalVatcodeUsed: string
    originalVatcodeUsedDescription: string
    vatGlAccountCredit: string
    vatGlAccountDebet: string
    vatGlAccountPurchases: string
    vatGlAccountSales: string
    revenuesGlAccount: string
    costsGlAccount: string
    plantCode: string
    materialTaxClassification: string
    customerTaxClassification: string
    invoiceLineNumber: string
    unitPrice: 0
    creditNoteReason: string
    generalLedgerId: string
    generalLedgerType: string
    journalDescription: string
    journalId: string
    journalType: string
    statisticalProcedure: string
    propertyCode: string
    propertyRegisterReference: string
    exemptReasonCode: string
    utilizationDate: 2019-05-23T21:00:10Z
    annualProrate: 0
    annualDeduction: 0
    annualDeductionEffectiveDate: 2019-05-23T21:00:10Z
    assetId: string
    deliveryIdentification: string
    firstSemester: true
    withholdingAmount: 0
    operationType: string
    profitCenter: string
    discountBaseAmount: 0
    businessArea: string
    costCenter: string
    materialNumber: string
    assignmentNumber: string
    projectNumber: string
    establishmentCode: string
    creationDate: 2019-05-23T21:00:10Z
    creationTime: string
    exchangeRate2: 0
    withholdingType: string
    withholdingRate: 0
    withholdingDescription: string
    salesOrderDate: 2019-05-23T21:00:10Z
    salesOrderNumber: string
    purchaseOrderNumber: string
    shipperCountryVATNumber: string
    shipperCountryVATNumberUsed: string
    shipperName: string
    shipperLocalCode: string
    shipmentType: string
    shipmentDescription: string
    shipmentWeightUOM: string
    shipmentWeightGross: 0
    shipmentWeightNet: 0
    shipmentDateTime: 2019-05-23T21:00:10Z
    itemCodeType: string
    itemCode: string
    transactionEndDate: 2019-05-23T21:00:10Z
    paymentExpireDate: 2019-05-23T21:00:10Z
    paymentBankName: string
    paymentCode: string
    intBankAccountNumber: string
    originalInvoiceDate: 2019-05-23T21:00:10Z
    shipmentNumofPackages: 0
    paymentDueDate: 0
    vatDueDate: string
    virtualStamp: string
    stampAmount: 0
    reaOffice: string
    reaNumber: string
    socialCapital: 0
    soleShareholder: string
    statusLiquidation: string
    referenceProvision: string
    doacupCode: string
    doacigCode: string
    dtCtrDocumentID: string
    dtCtrDate: 2019-05-23T21:00:10Z
    dtCtrItemNum: string
    dtCtrConvCode: string
    dtCtrCUPCode: string
    dtCtrCIGCode: string
    dtCnvDocumentID: string
    dtCnvDate: 2019-05-23T21:00:10Z
    dtCnvItemNum: string
    dtCnvConvCode: string
    dtCnvCUPCode: string
    dtCnvCIGCode: string
    dtRczDocumentID: string
    dtRczDate: 2019-05-23T21:00:10Z
    dtRczItemNum: string
    dtRczConvCode: string
    dtRczCUPCode: string
    dtRczCIGCode: string
    adGestionaliType: string
    adGestionaliText: string
    adGestionaliNumber: 0
    adGestionaliDate: 2019-05-23T21:00:10Z
    adGestionaliType2: string
    adGestionaliText2: string
    adGestionaliType3: string
    adGestionaliText3: string
    adGestionaliType4: string
    adGestionaliText4: string
    adGestionaliType5: string
    adGestionaliText5: string
    lineNature: string
    lineAdminReference: string
    shipmentCause: string
    shipTimeStamp: 2019-05-23T21:00:10Z
    shipmentStartDate: 2019-05-23T21:00:10Z
    alboProfessional: string
    alboProvince: string
    alboInscriptionDate: 2019-05-23T21:00:10Z
    supplierLocalOfficeAddress: string
    supplierLocalOfficeStreetNumber: string
    supplierLocalOfficePostalCode: 0
    supplierLocalOfficeCity: string
    supplierLocalOfficeProvince: string
    supplierLocalOfficeCountry: string
    supplierFiscalRepName: string
    supplierFiscalRepTIN: string
    supplierFiscalRepFirstName: string
    supplierFiscalRepLastName: string
    supplierFiscalRepCodEORI: string
    customerLocalOfficeAddress: string
    customerLocalOfficeStreetNumber: string
    customerLocalOfficePostalCode: 0
    customerLocalOfficeCity: string
    customerLocalOfficeProvince: string
    customerLocalOfficeCountry: string
    customerFiscalRepFirstName: string
    customerFiscalRepLastName: string
    roundingAmount: 0
    socSecType: string
    socSecRate: 0
    socSecContributionAmount: 0
    socSecTaxableAmount: 0
    socSecVATRate: 0
    socSecWithheld: string
    socSecNatura: string
    socSecAdminReference: string
    art73: string
    stageReference: 0
    shipperTIN: string
    driverFirstName: string
    driverLastName: string
    resaType: string
    mainInvoiceNumber: string
    mainInvoiceDate: 2019-05-23T21:00:10Z
    subjectWithheld: string
    additionalExpenses: 0
    paymentRoundingAmount: 0
    vehicleRegistrationDate: 2019-05-23T21:00:10Z
    vehicleTotalTravel: string
    paymentBeneficiary: string
    officePostalCode: string
    signerLastName: string
    signerFirstName: string
    signerTIN: string
    abiCode: 0
    cabCode: 0
    prepaymentDiscount: 0
    prepaymentDueDate: 2019-05-23T21:00:10Z
    penaltyLatePayment: 0
    penaltyStartDate: 2019-05-23T21:00:10Z
    supplierFiscalRepTitle: string
    driverTitle: string
    doaNumItem: string
    supplierFiscalRepCountryVATNumber: string
    customerFiscalRepCountryVATNumber: string
    salesOrderNumber2: string
    salesOrderNumber3: string
    salesOrderNumber4: string
    salesOrderNumber5: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ApiTransaction>
  <companyCode>string</companyCode>
  <invoiceNumber>string</invoiceNumber>
  <salesOrderNumber>string</salesOrderNumber>
  <purchaseOrderNumber>string</purchaseOrderNumber>
  <originalInvoiceNumber>string</originalInvoiceNumber>
  <currentApprovalStatus>string</currentApprovalStatus>
  <documentType>string</documentType>
  <sequencialNumberSalesBook>string</sequencialNumberSalesBook>
  <sequencialNumberPurchaseBook>string</sequencialNumberPurchaseBook>
  <transactionDate>2019-05-23T21:00:10Z</transactionDate>
  <intrastatDate>2019-05-23T21:00:10Z</intrastatDate>
  <invoiceDate>2019-05-23T21:00:10Z</invoiceDate>
  <paymentDate>2019-05-23T21:00:10Z</paymentDate>
  <reportDate>2019-05-23T21:00:10Z</reportDate>
  <invoiceType>string</invoiceType>
  <invoiceCorrectionType>string</invoiceCorrectionType>
  <invoiceSelfBilled>true</invoiceSelfBilled>
  <taxRegimeSales>string</taxRegimeSales>
  <taxRegimePurchases>string</taxRegimePurchases>
  <customsNumber>string</customsNumber>
  <customsDate>2019-05-23T21:00:10Z</customsDate>
  <paymentMethod>string</paymentMethod>
  <bankAccount>string</bankAccount>
  <transactionCode>string</transactionCode>
  <customsValue>string</customsValue>
  <erpDocument>string</erpDocument>
  <referenceId>string</referenceId>
  <creditIndicator>string</creditIndicator>
  <lastInvoiceNumber>string</lastInvoiceNumber>
  <transactionIsDeleted>true</transactionIsDeleted>
  <accountingDocumentNumber>string</accountingDocumentNumber>
  <glDescription>string</glDescription>
  <glPostingDate>2019-05-23T21:00:10Z</glPostingDate>
  <fiscalYear>string</fiscalYear>
  <fiscalPeriod>string</fiscalPeriod>
  <erpFiscalPeriod>string</erpFiscalPeriod>
  <erpFiscalYear>string</erpFiscalYear>
  <establishmentCode>string</establishmentCode>
  <environmentCode>string</environmentCode>
  <nFeNumber>string</nFeNumber>
  <nfNumber>string</nfNumber>
  <nFeServiceNumber>string</nFeServiceNumber>
  <nFeServiceIndicator>string</nFeServiceIndicator>
  <totalValue>0</totalValue>
  <totalValue2>0</totalValue2>
  <seriesNumber>string</seriesNumber>
  <issuerID>string</issuerID>
  <partialDeduct>0</partialDeduct>
  <typeOfService>string</typeOfService>
  <withholdingSubContractor>0</withholdingSubContractor>
  <withholdingExemption>0</withholdingExemption>
  <services15>0</services15>
  <services20>0</services20>
  <services25>0</services25>
  <additionalWithholdingExemption>0</additionalWithholdingExemption>
  <cprbIndicator>string</cprbIndicator>
  <customerIdType>string</customerIdType>
  <creationDate>2019-05-23T21:00:10Z</creationDate>
  <creationTime>string</creationTime>
  <reversalOperation>0</reversalOperation>
  <reversalFiscalYear>0</reversalFiscalYear>
  <reversalCompanyCode>string</reversalCompanyCode>
  <reversalAccountingDocument>string</reversalAccountingDocument>
  <externalReference>string</externalReference>
  <originalLineNumberReference>string</originalLineNumberReference>
  <registrationNumber>string</registrationNumber>
  <paymentConditions>string</paymentConditions>
  <supplierFiscalRepName>string</supplierFiscalRepName>
  <supplierFiscalRepAddress>string</supplierFiscalRepAddress>
  <supplierFiscalDescription>string</supplierFiscalDescription>
  <customerFiscalRepName>string</customerFiscalRepName>
  <customerFiscalRepAddress>string</customerFiscalRepAddress>
  <customerFiscalDescription>string</customerFiscalDescription>
  <supplierCertifiedEmail>string</supplierCertifiedEmail>
  <customerCertifiedEmail>string</customerCertifiedEmail>
  <supplierTIN>string</supplierTIN>
  <customerTIN>string</customerTIN>
  <supplierEORICode>string</supplierEORICode>
  <customerEORICode>string</customerEORICode>
  <supplierBIC>string</supplierBIC>
  <customer>
    <businessEntityID>string</businessEntityID>
    <name>string</name>
    <billToCountry>string</billToCountry>
    <vatNumberUsed>string</vatNumberUsed>
    <countryVatNumberUsed>string</countryVatNumberUsed>
    <billToStreet>string</billToStreet>
    <billToBuildingNumber>string</billToBuildingNumber>
    <billToCity>string</billToCity>
    <billToPostalCode>string</billToPostalCode>
    <ucr>string</ucr>
    <website>string</website>
    <billToAddressDetail>string</billToAddressDetail>
    <billToRegion>string</billToRegion>
    <billToStreetNumber>string</billToStreetNumber>
    <contactFirstName>string</contactFirstName>
    <contactLastName>string</contactLastName>
    <contactTitle>string</contactTitle>
    <contactVATNumber>string</contactVATNumber>
    <deliveryDate>2019-05-23T21:00:10Z</deliveryDate>
    <deliveryId>string</deliveryId>
    <emailAddress>string</emailAddress>
    <faxNumber>string</faxNumber>
    <shipFromAddressDetail>string</shipFromAddressDetail>
    <shipFromBuildingNumber>string</shipFromBuildingNumber>
    <shipFromCity>string</shipFromCity>
    <shipFromCountry>string</shipFromCountry>
    <shipFromLocationId>string</shipFromLocationId>
    <shipFromPostalCode>string</shipFromPostalCode>
    <shipFromRegion>string</shipFromRegion>
    <shipFromStreet>string</shipFromStreet>
    <shipFromStreetNumber>string</shipFromStreetNumber>
    <shipFromWarehouseId>string</shipFromWarehouseId>
    <shipToAddressDetail>string</shipToAddressDetail>
    <shipToBuildingNumber>string</shipToBuildingNumber>
    <shipToCity>string</shipToCity>
    <shipToCountry>string</shipToCountry>
    <shipToLocationId>string</shipToLocationId>
    <shipToPostalCode>string</shipToPostalCode>
    <shipToRegion>string</shipToRegion>
    <shipToStreet>string</shipToStreet>
    <shipToStreetNumber>string</shipToStreetNumber>
    <shipToWarehouseId>string</shipToWarehouseId>
    <telephoneNumber>string</telephoneNumber>
    <fiscalRepVATNumber>string</fiscalRepVATNumber>
    <idType>string</idType>
    <idNumber>string</idNumber>
    <localTaxNumber>string</localTaxNumber>
  </customer>
  <supplier>
    <invoiceNumber>string</invoiceNumber>
    <invoiceLineNumber>string</invoiceLineNumber>
    <originalInvoiceNumber>string</originalInvoiceNumber>
    <communicationType>string</communicationType>
    <businessEntityID>string</businessEntityID>
    <name>string</name>
    <billToCountry>string</billToCountry>
    <vatNumberUsed>string</vatNumberUsed>
    <countryVatNumberUsed>string</countryVatNumberUsed>
    <billToStreet>string</billToStreet>
    <billToBuildingNumber>string</billToBuildingNumber>
    <billToCity>string</billToCity>
    <billToPostalCode>string</billToPostalCode>
    <ucr>string</ucr>
    <website>string</website>
    <billToAddressDetail>string</billToAddressDetail>
    <billToRegion>string</billToRegion>
    <billToStreetNumber>string</billToStreetNumber>
    <contactFirstName>string</contactFirstName>
    <contactLastName>string</contactLastName>
    <contactTitle>string</contactTitle>
    <contactVATNumber>string</contactVATNumber>
    <deliveryDate>2019-05-23T21:00:10Z</deliveryDate>
    <deliveryId>string</deliveryId>
    <emailAddress>string</emailAddress>
    <faxNumber>string</faxNumber>
    <shipFromAddressDetail>string</shipFromAddressDetail>
    <shipFromBuildingNumber>string</shipFromBuildingNumber>
    <shipFromCity>string</shipFromCity>
    <shipFromCountry>string</shipFromCountry>
    <shipFromLocationId>string</shipFromLocationId>
    <shipFromPostalCode>string</shipFromPostalCode>
    <shipFromRegion>string</shipFromRegion>
    <shipFromStreet>string</shipFromStreet>
    <shipFromStreetNumber>string</shipFromStreetNumber>
    <shipFromWarehouseId>string</shipFromWarehouseId>
    <shipToAddressDetail>string</shipToAddressDetail>
    <shipToBuildingNumber>string</shipToBuildingNumber>
    <shipToCity>string</shipToCity>
    <shipToCountry>string</shipToCountry>
    <shipToLocationId>string</shipToLocationId>
    <shipToPostalCode>string</shipToPostalCode>
    <shipToRegion>string</shipToRegion>
    <shipToStreet>string</shipToStreet>
    <shipToStreetNumber>string</shipToStreetNumber>
    <shipToWarehouseId>string</shipToWarehouseId>
    <telephoneNumber>string</telephoneNumber>
    <fiscalRepVATNumber>string</fiscalRepVATNumber>
    <idType>string</idType>
    <idNumber>string</idNumber>
    <localTaxNumber>string</localTaxNumber>
  </supplier>
  <lines>
    <currency>string</currency>
    <currency2>string</currency2>
    <exchangeRate>0</exchangeRate>
    <vatCode>string</vatCode>
    <vatRate>string</vatRate>
    <itemDescription>string</itemDescription>
    <itemClassification>string</itemClassification>
    <taxableBasisCredit>0</taxableBasisCredit>
    <taxableBasisDebet>0</taxableBasisDebet>
    <valueVatCredit>0</valueVatCredit>
    <valueVatDebet>0</valueVatDebet>
    <totalValueLine>0</totalValueLine>
    <amountVatDeducted>0</amountVatDeducted>
    <taxableBasisCurrency2>0</taxableBasisCurrency2>
    <valueVatCurrency2>0</valueVatCurrency2>
    <totalValueLineCurrency2>0</totalValueLineCurrency2>
    <countryDispatch>string</countryDispatch>
    <countryArrival>string</countryArrival>
    <deliveryConditions>string</deliveryConditions>
    <additionalDocumentReference>string</additionalDocumentReference>
    <reportingType>string</reportingType>
    <transactionType>0</transactionType>
    <additionalTransactionType>0</additionalTransactionType>
    <intrastatCode>string</intrastatCode>
    <extrastatCode>string</extrastatCode>
    <additionalDescription>string</additionalDescription>
    <weight>0</weight>
    <unitOfMeasure>string</unitOfMeasure>
    <quantity>0</quantity>
    <additionalUnitOfMeasure>string</additionalUnitOfMeasure>
    <commercialValue>0</commercialValue>
    <statisticalValue>0</statisticalValue>
    <commercialValueCurrency2>0</commercialValueCurrency2>
    <statisticalValueCurrency2>0</statisticalValueCurrency2>
    <itemType>string</itemType>
    <modeOfTransport>0</modeOfTransport>
    <regionDispatch>string</regionDispatch>
    <harbourDispatch>string</harbourDispatch>
    <regionArrival>string</regionArrival>
    <harbourArrival>string</harbourArrival>
    <countryOrigin>string</countryOrigin>
    <purchaseExtra1>string</purchaseExtra1>
    <purchaseExtra2>string</purchaseExtra2>
    <purchaseExtra3>string</purchaseExtra3>
    <purchaseExtra4>string</purchaseExtra4>
    <purchaseExtra5>string</purchaseExtra5>
    <purchaseExtra6>string</purchaseExtra6>
    <purchaseExtra7>string</purchaseExtra7>
    <purchaseExtra8>string</purchaseExtra8>
    <purchaseExtra9>string</purchaseExtra9>
    <purchaseExtra10>string</purchaseExtra10>
    <salesExtra1>string</salesExtra1>
    <salesExtra2>string</salesExtra2>
    <salesExtra3>string</salesExtra3>
    <salesExtra4>string</salesExtra4>
    <salesExtra5>string</salesExtra5>
    <salesExtra6>string</salesExtra6>
    <salesExtra7>string</salesExtra7>
    <salesExtra8>string</salesExtra8>
    <salesExtra9>string</salesExtra9>
    <salesExtra10>string</salesExtra10>
    <mossReporterVatNumberUsed>string</mossReporterVatNumberUsed>
    <administrationCode>string</administrationCode>
    <vatCodeAssignerCode>string</vatCodeAssignerCode>
    <isOriginal>true</isOriginal>
    <deliveryConditionsPlace>string</deliveryConditionsPlace>
    <regionOrigin>string</regionOrigin>
    <vatCodeAccountingKey>string</vatCodeAccountingKey>
    <originalTaxRateApplied>string</originalTaxRateApplied>
    <originalVatcodeUsed>string</originalVatcodeUsed>
    <originalVatcodeUsedDescription>string</originalVatcodeUsedDescription>
    <vatGlAccountCredit>string</vatGlAccountCredit>
    <vatGlAccountDebet>string</vatGlAccountDebet>
    <vatGlAccountPurchases>string</vatGlAccountPurchases>
    <vatGlAccountSales>string</vatGlAccountSales>
    <revenuesGlAccount>string</revenuesGlAccount>
    <costsGlAccount>string</costsGlAccount>
    <plantCode>string</plantCode>
    <materialTaxClassification>string</materialTaxClassification>
    <customerTaxClassification>string</customerTaxClassification>
    <invoiceLineNumber>string</invoiceLineNumber>
    <unitPrice>0</unitPrice>
    <creditNoteReason>string</creditNoteReason>
    <generalLedgerId>string</generalLedgerId>
    <generalLedgerType>string</generalLedgerType>
    <journalDescription>string</journalDescription>
    <journalId>string</journalId>
    <journalType>string</journalType>
    <statisticalProcedure>string</statisticalProcedure>
    <propertyCode>string</propertyCode>
    <propertyRegisterReference>string</propertyRegisterReference>
    <exemptReasonCode>string</exemptReasonCode>
    <utilizationDate>2019-05-23T21:00:10Z</utilizationDate>
    <annualProrate>0</annualProrate>
    <annualDeduction>0</annualDeduction>
    <annualDeductionEffectiveDate>2019-05-23T21:00:10Z</annualDeductionEffectiveDate>
    <assetId>string</assetId>
    <deliveryIdentification>string</deliveryIdentification>
    <firstSemester>true</firstSemester>
    <withholdingAmount>0</withholdingAmount>
    <operationType>string</operationType>
    <profitCenter>string</profitCenter>
    <discountBaseAmount>0</discountBaseAmount>
    <businessArea>string</businessArea>
    <costCenter>string</costCenter>
    <materialNumber>string</materialNumber>
    <assignmentNumber>string</assignmentNumber>
    <projectNumber>string</projectNumber>
    <establishmentCode>string</establishmentCode>
    <creationDate>2019-05-23T21:00:10Z</creationDate>
    <creationTime>string</creationTime>
    <exchangeRate2>0</exchangeRate2>
    <withholdingType>string</withholdingType>
    <withholdingRate>0</withholdingRate>
    <withholdingDescription>string</withholdingDescription>
    <salesOrderDate>2019-05-23T21:00:10Z</salesOrderDate>
    <salesOrderNumber>string</salesOrderNumber>
    <purchaseOrderNumber>string</purchaseOrderNumber>
    <shipperCountryVATNumber>string</shipperCountryVATNumber>
    <shipperCountryVATNumberUsed>string</shipperCountryVATNumberUsed>
    <shipperName>string</shipperName>
    <shipperLocalCode>string</shipperLocalCode>
    <shipmentType>string</shipmentType>
    <shipmentDescription>string</shipmentDescription>
    <shipmentWeightUOM>string</shipmentWeightUOM>
    <shipmentWeightGross>0</shipmentWeightGross>
    <shipmentWeightNet>0</shipmentWeightNet>
    <shipmentDateTime>2019-05-23T21:00:10Z</shipmentDateTime>
    <itemCodeType>string</itemCodeType>
    <itemCode>string</itemCode>
    <transactionEndDate>2019-05-23T21:00:10Z</transactionEndDate>
    <paymentExpireDate>2019-05-23T21:00:10Z</paymentExpireDate>
    <paymentBankName>string</paymentBankName>
    <paymentCode>string</paymentCode>
    <intBankAccountNumber>string</intBankAccountNumber>
    <originalInvoiceDate>2019-05-23T21:00:10Z</originalInvoiceDate>
    <shipmentNumofPackages>0</shipmentNumofPackages>
    <paymentDueDate>0</paymentDueDate>
    <vatDueDate>string</vatDueDate>
    <virtualStamp>string</virtualStamp>
    <stampAmount>0</stampAmount>
    <reaOffice>string</reaOffice>
    <reaNumber>string</reaNumber>
    <socialCapital>0</socialCapital>
    <soleShareholder>string</soleShareholder>
    <statusLiquidation>string</statusLiquidation>
    <referenceProvision>string</referenceProvision>
    <doacupCode>string</doacupCode>
    <doacigCode>string</doacigCode>
    <dtCtrDocumentID>string</dtCtrDocumentID>
    <dtCtrDate>2019-05-23T21:00:10Z</dtCtrDate>
    <dtCtrItemNum>string</dtCtrItemNum>
    <dtCtrConvCode>string</dtCtrConvCode>
    <dtCtrCUPCode>string</dtCtrCUPCode>
    <dtCtrCIGCode>string</dtCtrCIGCode>
    <dtCnvDocumentID>string</dtCnvDocumentID>
    <dtCnvDate>2019-05-23T21:00:10Z</dtCnvDate>
    <dtCnvItemNum>string</dtCnvItemNum>
    <dtCnvConvCode>string</dtCnvConvCode>
    <dtCnvCUPCode>string</dtCnvCUPCode>
    <dtCnvCIGCode>string</dtCnvCIGCode>
    <dtRczDocumentID>string</dtRczDocumentID>
    <dtRczDate>2019-05-23T21:00:10Z</dtRczDate>
    <dtRczItemNum>string</dtRczItemNum>
    <dtRczConvCode>string</dtRczConvCode>
    <dtRczCUPCode>string</dtRczCUPCode>
    <dtRczCIGCode>string</dtRczCIGCode>
    <adGestionaliType>string</adGestionaliType>
    <adGestionaliText>string</adGestionaliText>
    <adGestionaliNumber>0</adGestionaliNumber>
    <adGestionaliDate>2019-05-23T21:00:10Z</adGestionaliDate>
    <adGestionaliType2>string</adGestionaliType2>
    <adGestionaliText2>string</adGestionaliText2>
    <adGestionaliType3>string</adGestionaliType3>
    <adGestionaliText3>string</adGestionaliText3>
    <adGestionaliType4>string</adGestionaliType4>
    <adGestionaliText4>string</adGestionaliText4>
    <adGestionaliType5>string</adGestionaliType5>
    <adGestionaliText5>string</adGestionaliText5>
    <lineNature>string</lineNature>
    <lineAdminReference>string</lineAdminReference>
    <shipmentCause>string</shipmentCause>
    <shipTimeStamp>2019-05-23T21:00:10Z</shipTimeStamp>
    <shipmentStartDate>2019-05-23T21:00:10Z</shipmentStartDate>
    <alboProfessional>string</alboProfessional>
    <alboProvince>string</alboProvince>
    <alboInscriptionDate>2019-05-23T21:00:10Z</alboInscriptionDate>
    <supplierLocalOfficeAddress>string</supplierLocalOfficeAddress>
    <supplierLocalOfficeStreetNumber>string</supplierLocalOfficeStreetNumber>
    <supplierLocalOfficePostalCode>0</supplierLocalOfficePostalCode>
    <supplierLocalOfficeCity>string</supplierLocalOfficeCity>
    <supplierLocalOfficeProvince>string</supplierLocalOfficeProvince>
    <supplierLocalOfficeCountry>string</supplierLocalOfficeCountry>
    <supplierFiscalRepName>string</supplierFiscalRepName>
    <supplierFiscalRepTIN>string</supplierFiscalRepTIN>
    <supplierFiscalRepFirstName>string</supplierFiscalRepFirstName>
    <supplierFiscalRepLastName>string</supplierFiscalRepLastName>
    <supplierFiscalRepCodEORI>string</supplierFiscalRepCodEORI>
    <customerLocalOfficeAddress>string</customerLocalOfficeAddress>
    <customerLocalOfficeStreetNumber>string</customerLocalOfficeStreetNumber>
    <customerLocalOfficePostalCode>0</customerLocalOfficePostalCode>
    <customerLocalOfficeCity>string</customerLocalOfficeCity>
    <customerLocalOfficeProvince>string</customerLocalOfficeProvince>
    <customerLocalOfficeCountry>string</customerLocalOfficeCountry>
    <customerFiscalRepFirstName>string</customerFiscalRepFirstName>
    <customerFiscalRepLastName>string</customerFiscalRepLastName>
    <roundingAmount>0</roundingAmount>
    <socSecType>string</socSecType>
    <socSecRate>0</socSecRate>
    <socSecContributionAmount>0</socSecContributionAmount>
    <socSecTaxableAmount>0</socSecTaxableAmount>
    <socSecVATRate>0</socSecVATRate>
    <socSecWithheld>string</socSecWithheld>
    <socSecNatura>string</socSecNatura>
    <socSecAdminReference>string</socSecAdminReference>
    <art73>string</art73>
    <stageReference>0</stageReference>
    <shipperTIN>string</shipperTIN>
    <driverFirstName>string</driverFirstName>
    <driverLastName>string</driverLastName>
    <resaType>string</resaType>
    <mainInvoiceNumber>string</mainInvoiceNumber>
    <mainInvoiceDate>2019-05-23T21:00:10Z</mainInvoiceDate>
    <subjectWithheld>string</subjectWithheld>
    <additionalExpenses>0</additionalExpenses>
    <paymentRoundingAmount>0</paymentRoundingAmount>
    <vehicleRegistrationDate>2019-05-23T21:00:10Z</vehicleRegistrationDate>
    <vehicleTotalTravel>string</vehicleTotalTravel>
    <paymentBeneficiary>string</paymentBeneficiary>
    <officePostalCode>string</officePostalCode>
    <signerLastName>string</signerLastName>
    <signerFirstName>string</signerFirstName>
    <signerTIN>string</signerTIN>
    <abiCode>0</abiCode>
    <cabCode>0</cabCode>
    <prepaymentDiscount>0</prepaymentDiscount>
    <prepaymentDueDate>2019-05-23T21:00:10Z</prepaymentDueDate>
    <penaltyLatePayment>0</penaltyLatePayment>
    <penaltyStartDate>2019-05-23T21:00:10Z</penaltyStartDate>
    <supplierFiscalRepTitle>string</supplierFiscalRepTitle>
    <driverTitle>string</driverTitle>
    <doaNumItem>string</doaNumItem>
    <supplierFiscalRepCountryVATNumber>string</supplierFiscalRepCountryVATNumber>
    <customerFiscalRepCountryVATNumber>string</customerFiscalRepCountryVATNumber>
    <salesOrderNumber2>string</salesOrderNumber2>
    <salesOrderNumber3>string</salesOrderNumber3>
    <salesOrderNumber4>string</salesOrderNumber4>
    <salesOrderNumber5>string</salesOrderNumber5>
  </lines>
</ApiTransaction>
```

<section>
<h3 id="transactionsv2_index-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ApiTransaction](#schemaapitransaction)|true|none|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="transactionsv2_index-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="transactionsv2_index-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

<section>

## Creates transactions

<a id="opIdTransactionsV2_Index"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://uatvat-api.sovos.com/api/v2/transactions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://uatvat-api.sovos.com/api/v2/transactions HTTP/1.1
Host: uatvat-api.sovos.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "entities": [
    {
      "name": "string",
      "fields": [
        {
          "name": "string",
          "value": {}
        }
      ],
      "entities": [
        null
      ]
    }
  ],
  "data": "string",
  "erpSystemId": "string",
  "actionsOverride": [
    "string"
  ],
  "importProfileName": "string",
  "messages": [
    {
      "description": "string",
      "legalStatusComments": "string",
      "legalTrackingId": "string",
      "processStartedTimestamp": "2019-05-23T21:00:10Z",
      "sendToErp": true
    }
  ],
  "attachments": [
    {
      "name": "string",
      "type": "string",
      "link": "string",
      "content": "string"
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://uatvat-api.sovos.com/api/v2/transactions',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://uatvat-api.sovos.com/api/v2/transactions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://uatvat-api.sovos.com/api/v2/transactions', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://uatvat-api.sovos.com/api/v2/transactions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://uatvat-api.sovos.com/api/v2/transactions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://uatvat-api.sovos.com/api/v2/transactions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/transactions`

> Body parameter

```json
{
  "entities": [
    {
      "name": "string",
      "fields": [
        {
          "name": "string",
          "value": {}
        }
      ],
      "entities": [
        null
      ]
    }
  ],
  "data": "string",
  "erpSystemId": "string",
  "actionsOverride": [
    "string"
  ],
  "importProfileName": "string",
  "messages": [
    {
      "description": "string",
      "legalStatusComments": "string",
      "legalTrackingId": "string",
      "processStartedTimestamp": "2019-05-23T21:00:10Z",
      "sendToErp": true
    }
  ],
  "attachments": [
    {
      "name": "string",
      "type": "string",
      "link": "string",
      "content": "string"
    }
  ]
}
```

```yaml
entities:
  - name: string
    fields:
      - name: string
        value: {}
    entities:
      - null
data: string
erpSystemId: string
actionsOverride:
  - string
importProfileName: string
messages:
  - description: string
    legalStatusComments: string
    legalTrackingId: string
    processStartedTimestamp: 2019-05-23T21:00:10Z
    sendToErp: true
attachments:
  - name: string
    type: string
    link: string
    content: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<EntitySpaceTransactionRequest>
  <entities>
    <name>string</name>
    <fields>
      <name>string</name>
      <value/>
    </fields>
    <entities/>
  </entities>
  <data>string</data>
  <erpSystemId>string</erpSystemId>
  <actionsOverride>string</actionsOverride>
  <importProfileName>string</importProfileName>
  <messages>
    <description>string</description>
    <legalStatusComments>string</legalStatusComments>
    <legalTrackingId>string</legalTrackingId>
    <processStartedTimestamp>2019-05-23T21:00:10Z</processStartedTimestamp>
    <sendToErp>true</sendToErp>
  </messages>
  <attachments>
    <name>string</name>
    <type>string</type>
    <link>string</link>
    <content>string</content>
  </attachments>
</EntitySpaceTransactionRequest>
```

<section>
<h3 id="creates-transactions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[EntitySpaceTransactionRequest](#schemaentityspacetransactionrequest)|true|max of 100 transactions to create|

</section>

> Example responses

> 200 Response

```json
{}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<section>
<h3 id="creates-transactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="creates-transactions-responseschema">Response Schema</h3>

</section>

<aside class="success">
This operation does not require authentication
</aside>

</section>

</section>

<section>

# Schemas

<section>
<h2 id="tocS_TransmissionServiceRequest">TransmissionServiceRequest</h2>
<!-- backwards compatibility -->
<a id="schematransmissionservicerequest"></a>
<a id="schema_TransmissionServiceRequest"></a>
<a id="tocStransmissionservicerequest"></a>
<a id="tocstransmissionservicerequest"></a>

```json
{
  "actionsOverride": [
    "string"
  ],
  "entities": [
    {
      "name": "string",
      "fields": [
        {
          "name": "string",
          "value": {}
        }
      ],
      "entities": [
        null
      ]
    }
  ],
  "messages": [
    {
      "status": 0,
      "category": "string",
      "code": "string",
      "description": "string",
      "legalStatusComments": "string",
      "legalTrackingId": "string",
      "processStartedTimestamp": "2019-05-23T21:00:10Z",
      "sendToErp": true
    }
  ],
  "attachments": [
    {
      "name": "string",
      "type": "string",
      "link": "string",
      "content": "string"
    }
  ]
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|actionsOverride|[string]|false|none|none|
|entities|[[TransmissionServiceEntity](#schematransmissionserviceentity)]|false|none|none|
|messages|[[TransmissionMessage](#schematransmissionmessage)]|false|none|none|
|attachments|[[TransmissionAttachment](#schematransmissionattachment)]|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_TransmissionServiceEntity">TransmissionServiceEntity</h2>
<!-- backwards compatibility -->
<a id="schematransmissionserviceentity"></a>
<a id="schema_TransmissionServiceEntity"></a>
<a id="tocStransmissionserviceentity"></a>
<a id="tocstransmissionserviceentity"></a>

```json
{
  "name": "string",
  "fields": [
    {
      "name": "string",
      "value": {}
    }
  ],
  "entities": [
    null
  ]
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|fields|[[TransmissionServiceField](#schematransmissionservicefield)]|false|none|none|
|entities|[[TransmissionServiceEntity](#schematransmissionserviceentity)]|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_TransmissionMessage">TransmissionMessage</h2>
<!-- backwards compatibility -->
<a id="schematransmissionmessage"></a>
<a id="schema_TransmissionMessage"></a>
<a id="tocStransmissionmessage"></a>
<a id="tocstransmissionmessage"></a>

```json
{
  "status": 0,
  "category": "string",
  "code": "string",
  "description": "string",
  "legalStatusComments": "string",
  "legalTrackingId": "string",
  "processStartedTimestamp": "2019-05-23T21:00:10Z",
  "sendToErp": true
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|status|integer(int32)|false|read-only|none|
|category|string|false|read-only|none|
|code|string|false|read-only|none|
|description|string|false|none|none|
|legalStatusComments|string|false|none|none|
|legalTrackingId|string|false|none|none|
|processStartedTimestamp|string(date-time)|false|none|none|
|sendToErp|boolean|false|none|none|

<section>

#### Enumerated Values

|Property|Value|
|---|---|
|status|0|
|status|1|
|status|2|

</section>

</section>
</section>

<section>
<h2 id="tocS_TransmissionAttachment">TransmissionAttachment</h2>
<!-- backwards compatibility -->
<a id="schematransmissionattachment"></a>
<a id="schema_TransmissionAttachment"></a>
<a id="tocStransmissionattachment"></a>
<a id="tocstransmissionattachment"></a>

```json
{
  "name": "string",
  "type": "string",
  "link": "string",
  "content": "string"
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|type|string|false|none|none|
|link|string|false|none|none|
|content|string|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_TransmissionServiceField">TransmissionServiceField</h2>
<!-- backwards compatibility -->
<a id="schematransmissionservicefield"></a>
<a id="schema_TransmissionServiceField"></a>
<a id="tocStransmissionservicefield"></a>
<a id="tocstransmissionservicefield"></a>

```json
{
  "name": "string",
  "value": {}
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|value|object|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiPageNotifications">ApiPageNotifications</h2>
<!-- backwards compatibility -->
<a id="schemaapipagenotifications"></a>
<a id="schema_ApiPageNotifications"></a>
<a id="tocSapipagenotifications"></a>
<a id="tocsapipagenotifications"></a>

```json
{
  "previous": "string",
  "next": "string",
  "totalPages": 0,
  "pageSize": 0,
  "startIndex": 0,
  "notifications": [
    {
      "notificationId": "string",
      "referenceId": "string",
      "companyCode": "string",
      "invoiceNumber": "string",
      "notificationCode": "string",
      "notificationDescription": "string",
      "notificationValue": "string",
      "notificationTimestamp": "2019-05-23T21:00:10Z",
      "acknowledgedNotification": true,
      "notificationProcessed": true,
      "companyName": "string",
      "notificationDateToDisplay": "string",
      "notificationOldValue": "string",
      "transactionField": "string",
      "notificationLink": "string",
      "erpDocument": "string",
      "environmentCode": "string"
    }
  ],
  "totalItems": 0
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|previous|string|false|none|none|
|next|string|false|none|none|
|totalPages|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|startIndex|integer(int32)|false|none|none|
|notifications|[[ApiNotification](#schemaapinotification)]|false|none|none|
|totalItems|integer(int32)|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiNotification">ApiNotification</h2>
<!-- backwards compatibility -->
<a id="schemaapinotification"></a>
<a id="schema_ApiNotification"></a>
<a id="tocSapinotification"></a>
<a id="tocsapinotification"></a>

```json
{
  "notificationId": "string",
  "referenceId": "string",
  "companyCode": "string",
  "invoiceNumber": "string",
  "notificationCode": "string",
  "notificationDescription": "string",
  "notificationValue": "string",
  "notificationTimestamp": "2019-05-23T21:00:10Z",
  "acknowledgedNotification": true,
  "notificationProcessed": true,
  "companyName": "string",
  "notificationDateToDisplay": "string",
  "notificationOldValue": "string",
  "transactionField": "string",
  "notificationLink": "string",
  "erpDocument": "string",
  "environmentCode": "string"
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|notificationId|string(uuid)|false|none|none|
|referenceId|string|false|none|none|
|companyCode|string|false|none|none|
|invoiceNumber|string|false|none|none|
|notificationCode|string|false|none|none|
|notificationDescription|string|false|none|none|
|notificationValue|string|false|none|none|
|notificationTimestamp|string(date-time)|false|none|none|
|acknowledgedNotification|boolean|false|none|none|
|notificationProcessed|boolean|false|none|none|
|companyName|string|false|none|none|
|notificationDateToDisplay|string|false|none|none|
|notificationOldValue|string|false|none|none|
|transactionField|string|false|none|none|
|notificationLink|string|false|none|none|
|erpDocument|string|false|none|none|
|environmentCode|string|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiNotificationV2Ack">ApiNotificationV2Ack</h2>
<!-- backwards compatibility -->
<a id="schemaapinotificationv2ack"></a>
<a id="schema_ApiNotificationV2Ack"></a>
<a id="tocSapinotificationv2ack"></a>
<a id="tocsapinotificationv2ack"></a>

```json
{
  "taxId": "string",
  "detail": [
    {
      "status": "string",
      "cloudId": "string"
    }
  ]
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxId|string|false|none|none|
|detail|[[ApiNotificationV2AckDetail](#schemaapinotificationv2ackdetail)]|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiNotificationV2AckDetail">ApiNotificationV2AckDetail</h2>
<!-- backwards compatibility -->
<a id="schemaapinotificationv2ackdetail"></a>
<a id="schema_ApiNotificationV2AckDetail"></a>
<a id="tocSapinotificationv2ackdetail"></a>
<a id="tocsapinotificationv2ackdetail"></a>

```json
{
  "status": "string",
  "cloudId": "string"
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|status|string|false|none|none|
|cloudId|string|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiTransactionRequest">ApiTransactionRequest</h2>
<!-- backwards compatibility -->
<a id="schemaapitransactionrequest"></a>
<a id="schema_ApiTransactionRequest"></a>
<a id="tocSapitransactionrequest"></a>
<a id="tocsapitransactionrequest"></a>

```json
{
  "importProfileName": "string",
  "fileName": "string",
  "customValues": {
    "property1": "string",
    "property2": "string"
  },
  "transactions": [
    {
      "companyCode": "string",
      "invoiceNumber": "string",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "originalInvoiceNumber": "string",
      "currentApprovalStatus": "string",
      "documentType": "string",
      "sequencialNumberSalesBook": "string",
      "sequencialNumberPurchaseBook": "string",
      "transactionDate": "2019-05-23T21:00:10Z",
      "intrastatDate": "2019-05-23T21:00:10Z",
      "invoiceDate": "2019-05-23T21:00:10Z",
      "paymentDate": "2019-05-23T21:00:10Z",
      "reportDate": "2019-05-23T21:00:10Z",
      "invoiceType": "string",
      "invoiceCorrectionType": "string",
      "invoiceSelfBilled": true,
      "taxRegimeSales": "string",
      "taxRegimePurchases": "string",
      "customsNumber": "string",
      "customsDate": "2019-05-23T21:00:10Z",
      "paymentMethod": "string",
      "bankAccount": "string",
      "transactionCode": "string",
      "customsValue": "string",
      "erpDocument": "string",
      "referenceId": "string",
      "creditIndicator": "string",
      "lastInvoiceNumber": "string",
      "transactionIsDeleted": true,
      "accountingDocumentNumber": "string",
      "glDescription": "string",
      "glPostingDate": "2019-05-23T21:00:10Z",
      "fiscalYear": "string",
      "fiscalPeriod": "string",
      "erpFiscalPeriod": "string",
      "erpFiscalYear": "string",
      "establishmentCode": "string",
      "environmentCode": "string",
      "nFeNumber": "string",
      "nfNumber": "string",
      "nFeServiceNumber": "string",
      "nFeServiceIndicator": "string",
      "totalValue": 0,
      "totalValue2": 0,
      "seriesNumber": "string",
      "issuerID": "string",
      "partialDeduct": 0,
      "typeOfService": "string",
      "withholdingSubContractor": 0,
      "withholdingExemption": 0,
      "services15": 0,
      "services20": 0,
      "services25": 0,
      "additionalWithholdingExemption": 0,
      "cprbIndicator": "string",
      "customerIdType": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "reversalOperation": 0,
      "reversalFiscalYear": 0,
      "reversalCompanyCode": "string",
      "reversalAccountingDocument": "string",
      "externalReference": "string",
      "originalLineNumberReference": "string",
      "registrationNumber": "string",
      "paymentConditions": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepAddress": "string",
      "supplierFiscalDescription": "string",
      "customerFiscalRepName": "string",
      "customerFiscalRepAddress": "string",
      "customerFiscalDescription": "string",
      "supplierCertifiedEmail": "string",
      "customerCertifiedEmail": "string",
      "supplierTIN": "string",
      "customerTIN": "string",
      "supplierEORICode": "string",
      "customerEORICode": "string",
      "supplierBIC": "string",
      "customer": {
        "businessEntityID": "string",
        "name": "string",
        "billToCountry": "string",
        "vatNumberUsed": "string",
        "countryVatNumberUsed": "string",
        "billToStreet": "string",
        "billToBuildingNumber": "string",
        "billToCity": "string",
        "billToPostalCode": "string",
        "ucr": "string",
        "website": "string",
        "billToAddressDetail": "string",
        "billToRegion": "string",
        "billToStreetNumber": "string",
        "contactFirstName": "string",
        "contactLastName": "string",
        "contactTitle": "string",
        "contactVATNumber": "string",
        "deliveryDate": "2019-05-23T21:00:10Z",
        "deliveryId": "string",
        "emailAddress": "string",
        "faxNumber": "string",
        "shipFromAddressDetail": "string",
        "shipFromBuildingNumber": "string",
        "shipFromCity": "string",
        "shipFromCountry": "string",
        "shipFromLocationId": "string",
        "shipFromPostalCode": "string",
        "shipFromRegion": "string",
        "shipFromStreet": "string",
        "shipFromStreetNumber": "string",
        "shipFromWarehouseId": "string",
        "shipToAddressDetail": "string",
        "shipToBuildingNumber": "string",
        "shipToCity": "string",
        "shipToCountry": "string",
        "shipToLocationId": "string",
        "shipToPostalCode": "string",
        "shipToRegion": "string",
        "shipToStreet": "string",
        "shipToStreetNumber": "string",
        "shipToWarehouseId": "string",
        "telephoneNumber": "string",
        "fiscalRepVATNumber": "string",
        "idType": "string",
        "idNumber": "string",
        "localTaxNumber": "string"
      },
      "supplier": {
        "invoiceNumber": "string",
        "invoiceLineNumber": "string",
        "originalInvoiceNumber": "string",
        "communicationType": "string",
        "businessEntityID": "string",
        "name": "string",
        "billToCountry": "string",
        "vatNumberUsed": "string",
        "countryVatNumberUsed": "string",
        "billToStreet": "string",
        "billToBuildingNumber": "string",
        "billToCity": "string",
        "billToPostalCode": "string",
        "ucr": "string",
        "website": "string",
        "billToAddressDetail": "string",
        "billToRegion": "string",
        "billToStreetNumber": "string",
        "contactFirstName": "string",
        "contactLastName": "string",
        "contactTitle": "string",
        "contactVATNumber": "string",
        "deliveryDate": "2019-05-23T21:00:10Z",
        "deliveryId": "string",
        "emailAddress": "string",
        "faxNumber": "string",
        "shipFromAddressDetail": "string",
        "shipFromBuildingNumber": "string",
        "shipFromCity": "string",
        "shipFromCountry": "string",
        "shipFromLocationId": "string",
        "shipFromPostalCode": "string",
        "shipFromRegion": "string",
        "shipFromStreet": "string",
        "shipFromStreetNumber": "string",
        "shipFromWarehouseId": "string",
        "shipToAddressDetail": "string",
        "shipToBuildingNumber": "string",
        "shipToCity": "string",
        "shipToCountry": "string",
        "shipToLocationId": "string",
        "shipToPostalCode": "string",
        "shipToRegion": "string",
        "shipToStreet": "string",
        "shipToStreetNumber": "string",
        "shipToWarehouseId": "string",
        "telephoneNumber": "string",
        "fiscalRepVATNumber": "string",
        "idType": "string",
        "idNumber": "string",
        "localTaxNumber": "string"
      },
      "lines": [
        {
          "currency": "string",
          "currency2": "string",
          "exchangeRate": 0,
          "vatCode": "string",
          "vatRate": "string",
          "itemDescription": "string",
          "itemClassification": "string",
          "taxableBasisCredit": 0,
          "taxableBasisDebet": 0,
          "valueVatCredit": 0,
          "valueVatDebet": 0,
          "totalValueLine": 0,
          "amountVatDeducted": 0,
          "taxableBasisCurrency2": 0,
          "valueVatCurrency2": 0,
          "totalValueLineCurrency2": 0,
          "countryDispatch": "string",
          "countryArrival": "string",
          "deliveryConditions": "string",
          "additionalDocumentReference": "string",
          "reportingType": "string",
          "transactionType": 0,
          "additionalTransactionType": 0,
          "intrastatCode": "string",
          "extrastatCode": "string",
          "additionalDescription": "string",
          "weight": 0,
          "unitOfMeasure": "string",
          "quantity": 0,
          "additionalUnitOfMeasure": "string",
          "commercialValue": 0,
          "statisticalValue": 0,
          "commercialValueCurrency2": 0,
          "statisticalValueCurrency2": 0,
          "itemType": "string",
          "modeOfTransport": 0,
          "regionDispatch": "string",
          "harbourDispatch": "string",
          "regionArrival": "string",
          "harbourArrival": "string",
          "countryOrigin": "string",
          "purchaseExtra1": "string",
          "purchaseExtra2": "string",
          "purchaseExtra3": "string",
          "purchaseExtra4": "string",
          "purchaseExtra5": "string",
          "purchaseExtra6": "string",
          "purchaseExtra7": "string",
          "purchaseExtra8": "string",
          "purchaseExtra9": "string",
          "purchaseExtra10": "string",
          "salesExtra1": "string",
          "salesExtra2": "string",
          "salesExtra3": "string",
          "salesExtra4": "string",
          "salesExtra5": "string",
          "salesExtra6": "string",
          "salesExtra7": "string",
          "salesExtra8": "string",
          "salesExtra9": "string",
          "salesExtra10": "string",
          "mossReporterVatNumberUsed": "string",
          "administrationCode": "string",
          "vatCodeAssignerCode": "string",
          "isOriginal": true,
          "deliveryConditionsPlace": "string",
          "regionOrigin": "string",
          "vatCodeAccountingKey": "string",
          "originalTaxRateApplied": "string",
          "originalVatcodeUsed": "string",
          "originalVatcodeUsedDescription": "string",
          "vatGlAccountCredit": "string",
          "vatGlAccountDebet": "string",
          "vatGlAccountPurchases": "string",
          "vatGlAccountSales": "string",
          "revenuesGlAccount": "string",
          "costsGlAccount": "string",
          "plantCode": "string",
          "materialTaxClassification": "string",
          "customerTaxClassification": "string",
          "invoiceLineNumber": "string",
          "unitPrice": 0,
          "creditNoteReason": "string",
          "generalLedgerId": "string",
          "generalLedgerType": "string",
          "journalDescription": "string",
          "journalId": "string",
          "journalType": "string",
          "statisticalProcedure": "string",
          "propertyCode": "string",
          "propertyRegisterReference": "string",
          "exemptReasonCode": "string",
          "utilizationDate": "2019-05-23T21:00:10Z",
          "annualProrate": 0,
          "annualDeduction": 0,
          "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
          "assetId": "string",
          "deliveryIdentification": "string",
          "firstSemester": true,
          "withholdingAmount": 0,
          "operationType": "string",
          "profitCenter": "string",
          "discountBaseAmount": 0,
          "businessArea": "string",
          "costCenter": "string",
          "materialNumber": "string",
          "assignmentNumber": "string",
          "projectNumber": "string",
          "establishmentCode": "string",
          "creationDate": "2019-05-23T21:00:10Z",
          "creationTime": "string",
          "exchangeRate2": 0,
          "withholdingType": "string",
          "withholdingRate": 0,
          "withholdingDescription": "string",
          "salesOrderDate": "2019-05-23T21:00:10Z",
          "salesOrderNumber": "string",
          "purchaseOrderNumber": "string",
          "shipperCountryVATNumber": "string",
          "shipperCountryVATNumberUsed": "string",
          "shipperName": "string",
          "shipperLocalCode": "string",
          "shipmentType": "string",
          "shipmentDescription": "string",
          "shipmentWeightUOM": "string",
          "shipmentWeightGross": 0,
          "shipmentWeightNet": 0,
          "shipmentDateTime": "2019-05-23T21:00:10Z",
          "itemCodeType": "string",
          "itemCode": "string",
          "transactionEndDate": "2019-05-23T21:00:10Z",
          "paymentExpireDate": "2019-05-23T21:00:10Z",
          "paymentBankName": "string",
          "paymentCode": "string",
          "intBankAccountNumber": "string",
          "originalInvoiceDate": "2019-05-23T21:00:10Z",
          "shipmentNumofPackages": 0,
          "paymentDueDate": 0,
          "vatDueDate": "string",
          "virtualStamp": "string",
          "stampAmount": 0,
          "reaOffice": "string",
          "reaNumber": "string",
          "socialCapital": 0,
          "soleShareholder": "string",
          "statusLiquidation": "string",
          "referenceProvision": "string",
          "doacupCode": "string",
          "doacigCode": "string",
          "dtCtrDocumentID": "string",
          "dtCtrDate": "2019-05-23T21:00:10Z",
          "dtCtrItemNum": "string",
          "dtCtrConvCode": "string",
          "dtCtrCUPCode": "string",
          "dtCtrCIGCode": "string",
          "dtCnvDocumentID": "string",
          "dtCnvDate": "2019-05-23T21:00:10Z",
          "dtCnvItemNum": "string",
          "dtCnvConvCode": "string",
          "dtCnvCUPCode": "string",
          "dtCnvCIGCode": "string",
          "dtRczDocumentID": "string",
          "dtRczDate": "2019-05-23T21:00:10Z",
          "dtRczItemNum": "string",
          "dtRczConvCode": "string",
          "dtRczCUPCode": "string",
          "dtRczCIGCode": "string",
          "adGestionaliType": "string",
          "adGestionaliText": "string",
          "adGestionaliNumber": 0,
          "adGestionaliDate": "2019-05-23T21:00:10Z",
          "adGestionaliType2": "string",
          "adGestionaliText2": "string",
          "adGestionaliType3": "string",
          "adGestionaliText3": "string",
          "adGestionaliType4": "string",
          "adGestionaliText4": "string",
          "adGestionaliType5": "string",
          "adGestionaliText5": "string",
          "lineNature": "string",
          "lineAdminReference": "string",
          "shipmentCause": "string",
          "shipTimeStamp": "2019-05-23T21:00:10Z",
          "shipmentStartDate": "2019-05-23T21:00:10Z",
          "alboProfessional": "string",
          "alboProvince": "string",
          "alboInscriptionDate": "2019-05-23T21:00:10Z",
          "supplierLocalOfficeAddress": "string",
          "supplierLocalOfficeStreetNumber": "string",
          "supplierLocalOfficePostalCode": 0,
          "supplierLocalOfficeCity": "string",
          "supplierLocalOfficeProvince": "string",
          "supplierLocalOfficeCountry": "string",
          "supplierFiscalRepName": "string",
          "supplierFiscalRepTIN": "string",
          "supplierFiscalRepFirstName": "string",
          "supplierFiscalRepLastName": "string",
          "supplierFiscalRepCodEORI": "string",
          "customerLocalOfficeAddress": "string",
          "customerLocalOfficeStreetNumber": "string",
          "customerLocalOfficePostalCode": 0,
          "customerLocalOfficeCity": "string",
          "customerLocalOfficeProvince": "string",
          "customerLocalOfficeCountry": "string",
          "customerFiscalRepFirstName": "string",
          "customerFiscalRepLastName": "string",
          "roundingAmount": 0,
          "socSecType": "string",
          "socSecRate": 0,
          "socSecContributionAmount": 0,
          "socSecTaxableAmount": 0,
          "socSecVATRate": 0,
          "socSecWithheld": "string",
          "socSecNatura": "string",
          "socSecAdminReference": "string",
          "art73": "string",
          "stageReference": 0,
          "shipperTIN": "string",
          "driverFirstName": "string",
          "driverLastName": "string",
          "resaType": "string",
          "mainInvoiceNumber": "string",
          "mainInvoiceDate": "2019-05-23T21:00:10Z",
          "subjectWithheld": "string",
          "additionalExpenses": 0,
          "paymentRoundingAmount": 0,
          "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
          "vehicleTotalTravel": "string",
          "paymentBeneficiary": "string",
          "officePostalCode": "string",
          "signerLastName": "string",
          "signerFirstName": "string",
          "signerTIN": "string",
          "abiCode": 0,
          "cabCode": 0,
          "prepaymentDiscount": 0,
          "prepaymentDueDate": "2019-05-23T21:00:10Z",
          "penaltyLatePayment": 0,
          "penaltyStartDate": "2019-05-23T21:00:10Z",
          "supplierFiscalRepTitle": "string",
          "driverTitle": "string",
          "doaNumItem": "string",
          "supplierFiscalRepCountryVATNumber": "string",
          "customerFiscalRepCountryVATNumber": "string",
          "salesOrderNumber2": "string",
          "salesOrderNumber3": "string",
          "salesOrderNumber4": "string",
          "salesOrderNumber5": "string"
        }
      ]
    }
  ]
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|importProfileName|string|false|none|none|
|fileName|string|false|none|none|
|customValues|object|false|none|none|
|» **additionalProperties**|string|false|none|none|
|transactions|[[ApiTransaction](#schemaapitransaction)]|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiTransaction">ApiTransaction</h2>
<!-- backwards compatibility -->
<a id="schemaapitransaction"></a>
<a id="schema_ApiTransaction"></a>
<a id="tocSapitransaction"></a>
<a id="tocsapitransaction"></a>

```json
{
  "companyCode": "string",
  "invoiceNumber": "string",
  "salesOrderNumber": "string",
  "purchaseOrderNumber": "string",
  "originalInvoiceNumber": "string",
  "currentApprovalStatus": "string",
  "documentType": "string",
  "sequencialNumberSalesBook": "string",
  "sequencialNumberPurchaseBook": "string",
  "transactionDate": "2019-05-23T21:00:10Z",
  "intrastatDate": "2019-05-23T21:00:10Z",
  "invoiceDate": "2019-05-23T21:00:10Z",
  "paymentDate": "2019-05-23T21:00:10Z",
  "reportDate": "2019-05-23T21:00:10Z",
  "invoiceType": "string",
  "invoiceCorrectionType": "string",
  "invoiceSelfBilled": true,
  "taxRegimeSales": "string",
  "taxRegimePurchases": "string",
  "customsNumber": "string",
  "customsDate": "2019-05-23T21:00:10Z",
  "paymentMethod": "string",
  "bankAccount": "string",
  "transactionCode": "string",
  "customsValue": "string",
  "erpDocument": "string",
  "referenceId": "string",
  "creditIndicator": "string",
  "lastInvoiceNumber": "string",
  "transactionIsDeleted": true,
  "accountingDocumentNumber": "string",
  "glDescription": "string",
  "glPostingDate": "2019-05-23T21:00:10Z",
  "fiscalYear": "string",
  "fiscalPeriod": "string",
  "erpFiscalPeriod": "string",
  "erpFiscalYear": "string",
  "establishmentCode": "string",
  "environmentCode": "string",
  "nFeNumber": "string",
  "nfNumber": "string",
  "nFeServiceNumber": "string",
  "nFeServiceIndicator": "string",
  "totalValue": 0,
  "totalValue2": 0,
  "seriesNumber": "string",
  "issuerID": "string",
  "partialDeduct": 0,
  "typeOfService": "string",
  "withholdingSubContractor": 0,
  "withholdingExemption": 0,
  "services15": 0,
  "services20": 0,
  "services25": 0,
  "additionalWithholdingExemption": 0,
  "cprbIndicator": "string",
  "customerIdType": "string",
  "creationDate": "2019-05-23T21:00:10Z",
  "creationTime": "string",
  "reversalOperation": 0,
  "reversalFiscalYear": 0,
  "reversalCompanyCode": "string",
  "reversalAccountingDocument": "string",
  "externalReference": "string",
  "originalLineNumberReference": "string",
  "registrationNumber": "string",
  "paymentConditions": "string",
  "supplierFiscalRepName": "string",
  "supplierFiscalRepAddress": "string",
  "supplierFiscalDescription": "string",
  "customerFiscalRepName": "string",
  "customerFiscalRepAddress": "string",
  "customerFiscalDescription": "string",
  "supplierCertifiedEmail": "string",
  "customerCertifiedEmail": "string",
  "supplierTIN": "string",
  "customerTIN": "string",
  "supplierEORICode": "string",
  "customerEORICode": "string",
  "supplierBIC": "string",
  "customer": {
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "supplier": {
    "invoiceNumber": "string",
    "invoiceLineNumber": "string",
    "originalInvoiceNumber": "string",
    "communicationType": "string",
    "businessEntityID": "string",
    "name": "string",
    "billToCountry": "string",
    "vatNumberUsed": "string",
    "countryVatNumberUsed": "string",
    "billToStreet": "string",
    "billToBuildingNumber": "string",
    "billToCity": "string",
    "billToPostalCode": "string",
    "ucr": "string",
    "website": "string",
    "billToAddressDetail": "string",
    "billToRegion": "string",
    "billToStreetNumber": "string",
    "contactFirstName": "string",
    "contactLastName": "string",
    "contactTitle": "string",
    "contactVATNumber": "string",
    "deliveryDate": "2019-05-23T21:00:10Z",
    "deliveryId": "string",
    "emailAddress": "string",
    "faxNumber": "string",
    "shipFromAddressDetail": "string",
    "shipFromBuildingNumber": "string",
    "shipFromCity": "string",
    "shipFromCountry": "string",
    "shipFromLocationId": "string",
    "shipFromPostalCode": "string",
    "shipFromRegion": "string",
    "shipFromStreet": "string",
    "shipFromStreetNumber": "string",
    "shipFromWarehouseId": "string",
    "shipToAddressDetail": "string",
    "shipToBuildingNumber": "string",
    "shipToCity": "string",
    "shipToCountry": "string",
    "shipToLocationId": "string",
    "shipToPostalCode": "string",
    "shipToRegion": "string",
    "shipToStreet": "string",
    "shipToStreetNumber": "string",
    "shipToWarehouseId": "string",
    "telephoneNumber": "string",
    "fiscalRepVATNumber": "string",
    "idType": "string",
    "idNumber": "string",
    "localTaxNumber": "string"
  },
  "lines": [
    {
      "currency": "string",
      "currency2": "string",
      "exchangeRate": 0,
      "vatCode": "string",
      "vatRate": "string",
      "itemDescription": "string",
      "itemClassification": "string",
      "taxableBasisCredit": 0,
      "taxableBasisDebet": 0,
      "valueVatCredit": 0,
      "valueVatDebet": 0,
      "totalValueLine": 0,
      "amountVatDeducted": 0,
      "taxableBasisCurrency2": 0,
      "valueVatCurrency2": 0,
      "totalValueLineCurrency2": 0,
      "countryDispatch": "string",
      "countryArrival": "string",
      "deliveryConditions": "string",
      "additionalDocumentReference": "string",
      "reportingType": "string",
      "transactionType": 0,
      "additionalTransactionType": 0,
      "intrastatCode": "string",
      "extrastatCode": "string",
      "additionalDescription": "string",
      "weight": 0,
      "unitOfMeasure": "string",
      "quantity": 0,
      "additionalUnitOfMeasure": "string",
      "commercialValue": 0,
      "statisticalValue": 0,
      "commercialValueCurrency2": 0,
      "statisticalValueCurrency2": 0,
      "itemType": "string",
      "modeOfTransport": 0,
      "regionDispatch": "string",
      "harbourDispatch": "string",
      "regionArrival": "string",
      "harbourArrival": "string",
      "countryOrigin": "string",
      "purchaseExtra1": "string",
      "purchaseExtra2": "string",
      "purchaseExtra3": "string",
      "purchaseExtra4": "string",
      "purchaseExtra5": "string",
      "purchaseExtra6": "string",
      "purchaseExtra7": "string",
      "purchaseExtra8": "string",
      "purchaseExtra9": "string",
      "purchaseExtra10": "string",
      "salesExtra1": "string",
      "salesExtra2": "string",
      "salesExtra3": "string",
      "salesExtra4": "string",
      "salesExtra5": "string",
      "salesExtra6": "string",
      "salesExtra7": "string",
      "salesExtra8": "string",
      "salesExtra9": "string",
      "salesExtra10": "string",
      "mossReporterVatNumberUsed": "string",
      "administrationCode": "string",
      "vatCodeAssignerCode": "string",
      "isOriginal": true,
      "deliveryConditionsPlace": "string",
      "regionOrigin": "string",
      "vatCodeAccountingKey": "string",
      "originalTaxRateApplied": "string",
      "originalVatcodeUsed": "string",
      "originalVatcodeUsedDescription": "string",
      "vatGlAccountCredit": "string",
      "vatGlAccountDebet": "string",
      "vatGlAccountPurchases": "string",
      "vatGlAccountSales": "string",
      "revenuesGlAccount": "string",
      "costsGlAccount": "string",
      "plantCode": "string",
      "materialTaxClassification": "string",
      "customerTaxClassification": "string",
      "invoiceLineNumber": "string",
      "unitPrice": 0,
      "creditNoteReason": "string",
      "generalLedgerId": "string",
      "generalLedgerType": "string",
      "journalDescription": "string",
      "journalId": "string",
      "journalType": "string",
      "statisticalProcedure": "string",
      "propertyCode": "string",
      "propertyRegisterReference": "string",
      "exemptReasonCode": "string",
      "utilizationDate": "2019-05-23T21:00:10Z",
      "annualProrate": 0,
      "annualDeduction": 0,
      "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
      "assetId": "string",
      "deliveryIdentification": "string",
      "firstSemester": true,
      "withholdingAmount": 0,
      "operationType": "string",
      "profitCenter": "string",
      "discountBaseAmount": 0,
      "businessArea": "string",
      "costCenter": "string",
      "materialNumber": "string",
      "assignmentNumber": "string",
      "projectNumber": "string",
      "establishmentCode": "string",
      "creationDate": "2019-05-23T21:00:10Z",
      "creationTime": "string",
      "exchangeRate2": 0,
      "withholdingType": "string",
      "withholdingRate": 0,
      "withholdingDescription": "string",
      "salesOrderDate": "2019-05-23T21:00:10Z",
      "salesOrderNumber": "string",
      "purchaseOrderNumber": "string",
      "shipperCountryVATNumber": "string",
      "shipperCountryVATNumberUsed": "string",
      "shipperName": "string",
      "shipperLocalCode": "string",
      "shipmentType": "string",
      "shipmentDescription": "string",
      "shipmentWeightUOM": "string",
      "shipmentWeightGross": 0,
      "shipmentWeightNet": 0,
      "shipmentDateTime": "2019-05-23T21:00:10Z",
      "itemCodeType": "string",
      "itemCode": "string",
      "transactionEndDate": "2019-05-23T21:00:10Z",
      "paymentExpireDate": "2019-05-23T21:00:10Z",
      "paymentBankName": "string",
      "paymentCode": "string",
      "intBankAccountNumber": "string",
      "originalInvoiceDate": "2019-05-23T21:00:10Z",
      "shipmentNumofPackages": 0,
      "paymentDueDate": 0,
      "vatDueDate": "string",
      "virtualStamp": "string",
      "stampAmount": 0,
      "reaOffice": "string",
      "reaNumber": "string",
      "socialCapital": 0,
      "soleShareholder": "string",
      "statusLiquidation": "string",
      "referenceProvision": "string",
      "doacupCode": "string",
      "doacigCode": "string",
      "dtCtrDocumentID": "string",
      "dtCtrDate": "2019-05-23T21:00:10Z",
      "dtCtrItemNum": "string",
      "dtCtrConvCode": "string",
      "dtCtrCUPCode": "string",
      "dtCtrCIGCode": "string",
      "dtCnvDocumentID": "string",
      "dtCnvDate": "2019-05-23T21:00:10Z",
      "dtCnvItemNum": "string",
      "dtCnvConvCode": "string",
      "dtCnvCUPCode": "string",
      "dtCnvCIGCode": "string",
      "dtRczDocumentID": "string",
      "dtRczDate": "2019-05-23T21:00:10Z",
      "dtRczItemNum": "string",
      "dtRczConvCode": "string",
      "dtRczCUPCode": "string",
      "dtRczCIGCode": "string",
      "adGestionaliType": "string",
      "adGestionaliText": "string",
      "adGestionaliNumber": 0,
      "adGestionaliDate": "2019-05-23T21:00:10Z",
      "adGestionaliType2": "string",
      "adGestionaliText2": "string",
      "adGestionaliType3": "string",
      "adGestionaliText3": "string",
      "adGestionaliType4": "string",
      "adGestionaliText4": "string",
      "adGestionaliType5": "string",
      "adGestionaliText5": "string",
      "lineNature": "string",
      "lineAdminReference": "string",
      "shipmentCause": "string",
      "shipTimeStamp": "2019-05-23T21:00:10Z",
      "shipmentStartDate": "2019-05-23T21:00:10Z",
      "alboProfessional": "string",
      "alboProvince": "string",
      "alboInscriptionDate": "2019-05-23T21:00:10Z",
      "supplierLocalOfficeAddress": "string",
      "supplierLocalOfficeStreetNumber": "string",
      "supplierLocalOfficePostalCode": 0,
      "supplierLocalOfficeCity": "string",
      "supplierLocalOfficeProvince": "string",
      "supplierLocalOfficeCountry": "string",
      "supplierFiscalRepName": "string",
      "supplierFiscalRepTIN": "string",
      "supplierFiscalRepFirstName": "string",
      "supplierFiscalRepLastName": "string",
      "supplierFiscalRepCodEORI": "string",
      "customerLocalOfficeAddress": "string",
      "customerLocalOfficeStreetNumber": "string",
      "customerLocalOfficePostalCode": 0,
      "customerLocalOfficeCity": "string",
      "customerLocalOfficeProvince": "string",
      "customerLocalOfficeCountry": "string",
      "customerFiscalRepFirstName": "string",
      "customerFiscalRepLastName": "string",
      "roundingAmount": 0,
      "socSecType": "string",
      "socSecRate": 0,
      "socSecContributionAmount": 0,
      "socSecTaxableAmount": 0,
      "socSecVATRate": 0,
      "socSecWithheld": "string",
      "socSecNatura": "string",
      "socSecAdminReference": "string",
      "art73": "string",
      "stageReference": 0,
      "shipperTIN": "string",
      "driverFirstName": "string",
      "driverLastName": "string",
      "resaType": "string",
      "mainInvoiceNumber": "string",
      "mainInvoiceDate": "2019-05-23T21:00:10Z",
      "subjectWithheld": "string",
      "additionalExpenses": 0,
      "paymentRoundingAmount": 0,
      "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
      "vehicleTotalTravel": "string",
      "paymentBeneficiary": "string",
      "officePostalCode": "string",
      "signerLastName": "string",
      "signerFirstName": "string",
      "signerTIN": "string",
      "abiCode": 0,
      "cabCode": 0,
      "prepaymentDiscount": 0,
      "prepaymentDueDate": "2019-05-23T21:00:10Z",
      "penaltyLatePayment": 0,
      "penaltyStartDate": "2019-05-23T21:00:10Z",
      "supplierFiscalRepTitle": "string",
      "driverTitle": "string",
      "doaNumItem": "string",
      "supplierFiscalRepCountryVATNumber": "string",
      "customerFiscalRepCountryVATNumber": "string",
      "salesOrderNumber2": "string",
      "salesOrderNumber3": "string",
      "salesOrderNumber4": "string",
      "salesOrderNumber5": "string"
    }
  ]
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|companyCode|string|false|none|none|
|invoiceNumber|string|false|none|none|
|salesOrderNumber|string|false|none|none|
|purchaseOrderNumber|string|false|none|none|
|originalInvoiceNumber|string|false|none|none|
|currentApprovalStatus|string|false|none|none|
|documentType|string|false|none|none|
|sequencialNumberSalesBook|string|false|none|none|
|sequencialNumberPurchaseBook|string|false|none|none|
|transactionDate|string(date-time)|false|none|none|
|intrastatDate|string(date-time)|false|none|none|
|invoiceDate|string(date-time)|false|none|none|
|paymentDate|string(date-time)|false|none|none|
|reportDate|string(date-time)|false|none|none|
|invoiceType|string|false|none|none|
|invoiceCorrectionType|string|false|none|none|
|invoiceSelfBilled|boolean|false|none|none|
|taxRegimeSales|string|false|none|none|
|taxRegimePurchases|string|false|none|none|
|customsNumber|string|false|none|none|
|customsDate|string(date-time)|false|none|none|
|paymentMethod|string|false|none|none|
|bankAccount|string|false|none|none|
|transactionCode|string|false|none|none|
|customsValue|string|false|none|none|
|erpDocument|string|false|none|none|
|referenceId|string|false|none|none|
|creditIndicator|string|false|none|none|
|lastInvoiceNumber|string|false|none|none|
|transactionIsDeleted|boolean|false|none|none|
|accountingDocumentNumber|string|false|none|none|
|glDescription|string|false|none|none|
|glPostingDate|string(date-time)|false|none|none|
|fiscalYear|string|false|none|none|
|fiscalPeriod|string|false|none|none|
|erpFiscalPeriod|string|false|none|none|
|erpFiscalYear|string|false|none|none|
|establishmentCode|string|false|none|none|
|environmentCode|string|false|none|none|
|nFeNumber|string|false|none|none|
|nfNumber|string|false|none|none|
|nFeServiceNumber|string|false|none|none|
|nFeServiceIndicator|string|false|none|none|
|totalValue|number(double)|false|none|none|
|totalValue2|number(double)|false|none|none|
|seriesNumber|string|false|none|none|
|issuerID|string|false|none|none|
|partialDeduct|number(double)|false|none|none|
|typeOfService|string|false|none|none|
|withholdingSubContractor|number(double)|false|none|none|
|withholdingExemption|number(double)|false|none|none|
|services15|number(double)|false|none|none|
|services20|number(double)|false|none|none|
|services25|number(double)|false|none|none|
|additionalWithholdingExemption|number(double)|false|none|none|
|cprbIndicator|string|false|none|none|
|customerIdType|string|false|none|none|
|creationDate|string(date-time)|false|none|none|
|creationTime|string|false|none|none|
|reversalOperation|integer(int32)|false|none|none|
|reversalFiscalYear|integer(int32)|false|none|none|
|reversalCompanyCode|string|false|none|none|
|reversalAccountingDocument|string|false|none|none|
|externalReference|string|false|none|none|
|originalLineNumberReference|string|false|none|none|
|registrationNumber|string|false|none|none|
|paymentConditions|string|false|none|none|
|supplierFiscalRepName|string|false|none|none|
|supplierFiscalRepAddress|string|false|none|none|
|supplierFiscalDescription|string|false|none|none|
|customerFiscalRepName|string|false|none|none|
|customerFiscalRepAddress|string|false|none|none|
|customerFiscalDescription|string|false|none|none|
|supplierCertifiedEmail|string|false|none|none|
|customerCertifiedEmail|string|false|none|none|
|supplierTIN|string|false|none|none|
|customerTIN|string|false|none|none|
|supplierEORICode|string|false|none|none|
|customerEORICode|string|false|none|none|
|supplierBIC|string|false|none|none|
|customer|[ApiCustomer](#schemaapicustomer)|false|none|none|
|supplier|[ApiSupplier](#schemaapisupplier)|false|none|none|
|lines|[[ApiTransactionLine](#schemaapitransactionline)]|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiCustomer">ApiCustomer</h2>
<!-- backwards compatibility -->
<a id="schemaapicustomer"></a>
<a id="schema_ApiCustomer"></a>
<a id="tocSapicustomer"></a>
<a id="tocsapicustomer"></a>

```json
{
  "businessEntityID": "string",
  "name": "string",
  "billToCountry": "string",
  "vatNumberUsed": "string",
  "countryVatNumberUsed": "string",
  "billToStreet": "string",
  "billToBuildingNumber": "string",
  "billToCity": "string",
  "billToPostalCode": "string",
  "ucr": "string",
  "website": "string",
  "billToAddressDetail": "string",
  "billToRegion": "string",
  "billToStreetNumber": "string",
  "contactFirstName": "string",
  "contactLastName": "string",
  "contactTitle": "string",
  "contactVATNumber": "string",
  "deliveryDate": "2019-05-23T21:00:10Z",
  "deliveryId": "string",
  "emailAddress": "string",
  "faxNumber": "string",
  "shipFromAddressDetail": "string",
  "shipFromBuildingNumber": "string",
  "shipFromCity": "string",
  "shipFromCountry": "string",
  "shipFromLocationId": "string",
  "shipFromPostalCode": "string",
  "shipFromRegion": "string",
  "shipFromStreet": "string",
  "shipFromStreetNumber": "string",
  "shipFromWarehouseId": "string",
  "shipToAddressDetail": "string",
  "shipToBuildingNumber": "string",
  "shipToCity": "string",
  "shipToCountry": "string",
  "shipToLocationId": "string",
  "shipToPostalCode": "string",
  "shipToRegion": "string",
  "shipToStreet": "string",
  "shipToStreetNumber": "string",
  "shipToWarehouseId": "string",
  "telephoneNumber": "string",
  "fiscalRepVATNumber": "string",
  "idType": "string",
  "idNumber": "string",
  "localTaxNumber": "string"
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|businessEntityID|string|false|none|none|
|name|string|false|none|none|
|billToCountry|string|false|none|none|
|vatNumberUsed|string|false|none|none|
|countryVatNumberUsed|string|false|none|none|
|billToStreet|string|false|none|none|
|billToBuildingNumber|string|false|none|none|
|billToCity|string|false|none|none|
|billToPostalCode|string|false|none|none|
|ucr|string|false|none|none|
|website|string|false|none|none|
|billToAddressDetail|string|false|none|none|
|billToRegion|string|false|none|none|
|billToStreetNumber|string|false|none|none|
|contactFirstName|string|false|none|none|
|contactLastName|string|false|none|none|
|contactTitle|string|false|none|none|
|contactVATNumber|string|false|none|none|
|deliveryDate|string(date-time)|false|none|none|
|deliveryId|string|false|none|none|
|emailAddress|string|false|none|none|
|faxNumber|string|false|none|none|
|shipFromAddressDetail|string|false|none|none|
|shipFromBuildingNumber|string|false|none|none|
|shipFromCity|string|false|none|none|
|shipFromCountry|string|false|none|none|
|shipFromLocationId|string|false|none|none|
|shipFromPostalCode|string|false|none|none|
|shipFromRegion|string|false|none|none|
|shipFromStreet|string|false|none|none|
|shipFromStreetNumber|string|false|none|none|
|shipFromWarehouseId|string|false|none|none|
|shipToAddressDetail|string|false|none|none|
|shipToBuildingNumber|string|false|none|none|
|shipToCity|string|false|none|none|
|shipToCountry|string|false|none|none|
|shipToLocationId|string|false|none|none|
|shipToPostalCode|string|false|none|none|
|shipToRegion|string|false|none|none|
|shipToStreet|string|false|none|none|
|shipToStreetNumber|string|false|none|none|
|shipToWarehouseId|string|false|none|none|
|telephoneNumber|string|false|none|none|
|fiscalRepVATNumber|string|false|none|none|
|idType|string|false|none|none|
|idNumber|string|false|none|none|
|localTaxNumber|string|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiSupplier">ApiSupplier</h2>
<!-- backwards compatibility -->
<a id="schemaapisupplier"></a>
<a id="schema_ApiSupplier"></a>
<a id="tocSapisupplier"></a>
<a id="tocsapisupplier"></a>

```json
{
  "invoiceNumber": "string",
  "invoiceLineNumber": "string",
  "originalInvoiceNumber": "string",
  "communicationType": "string",
  "businessEntityID": "string",
  "name": "string",
  "billToCountry": "string",
  "vatNumberUsed": "string",
  "countryVatNumberUsed": "string",
  "billToStreet": "string",
  "billToBuildingNumber": "string",
  "billToCity": "string",
  "billToPostalCode": "string",
  "ucr": "string",
  "website": "string",
  "billToAddressDetail": "string",
  "billToRegion": "string",
  "billToStreetNumber": "string",
  "contactFirstName": "string",
  "contactLastName": "string",
  "contactTitle": "string",
  "contactVATNumber": "string",
  "deliveryDate": "2019-05-23T21:00:10Z",
  "deliveryId": "string",
  "emailAddress": "string",
  "faxNumber": "string",
  "shipFromAddressDetail": "string",
  "shipFromBuildingNumber": "string",
  "shipFromCity": "string",
  "shipFromCountry": "string",
  "shipFromLocationId": "string",
  "shipFromPostalCode": "string",
  "shipFromRegion": "string",
  "shipFromStreet": "string",
  "shipFromStreetNumber": "string",
  "shipFromWarehouseId": "string",
  "shipToAddressDetail": "string",
  "shipToBuildingNumber": "string",
  "shipToCity": "string",
  "shipToCountry": "string",
  "shipToLocationId": "string",
  "shipToPostalCode": "string",
  "shipToRegion": "string",
  "shipToStreet": "string",
  "shipToStreetNumber": "string",
  "shipToWarehouseId": "string",
  "telephoneNumber": "string",
  "fiscalRepVATNumber": "string",
  "idType": "string",
  "idNumber": "string",
  "localTaxNumber": "string"
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|invoiceNumber|string|false|none|none|
|invoiceLineNumber|string|false|none|none|
|originalInvoiceNumber|string|false|none|none|
|communicationType|string|false|none|none|
|businessEntityID|string|false|none|none|
|name|string|false|none|none|
|billToCountry|string|false|none|none|
|vatNumberUsed|string|false|none|none|
|countryVatNumberUsed|string|false|none|none|
|billToStreet|string|false|none|none|
|billToBuildingNumber|string|false|none|none|
|billToCity|string|false|none|none|
|billToPostalCode|string|false|none|none|
|ucr|string|false|none|none|
|website|string|false|none|none|
|billToAddressDetail|string|false|none|none|
|billToRegion|string|false|none|none|
|billToStreetNumber|string|false|none|none|
|contactFirstName|string|false|none|none|
|contactLastName|string|false|none|none|
|contactTitle|string|false|none|none|
|contactVATNumber|string|false|none|none|
|deliveryDate|string(date-time)|false|none|none|
|deliveryId|string|false|none|none|
|emailAddress|string|false|none|none|
|faxNumber|string|false|none|none|
|shipFromAddressDetail|string|false|none|none|
|shipFromBuildingNumber|string|false|none|none|
|shipFromCity|string|false|none|none|
|shipFromCountry|string|false|none|none|
|shipFromLocationId|string|false|none|none|
|shipFromPostalCode|string|false|none|none|
|shipFromRegion|string|false|none|none|
|shipFromStreet|string|false|none|none|
|shipFromStreetNumber|string|false|none|none|
|shipFromWarehouseId|string|false|none|none|
|shipToAddressDetail|string|false|none|none|
|shipToBuildingNumber|string|false|none|none|
|shipToCity|string|false|none|none|
|shipToCountry|string|false|none|none|
|shipToLocationId|string|false|none|none|
|shipToPostalCode|string|false|none|none|
|shipToRegion|string|false|none|none|
|shipToStreet|string|false|none|none|
|shipToStreetNumber|string|false|none|none|
|shipToWarehouseId|string|false|none|none|
|telephoneNumber|string|false|none|none|
|fiscalRepVATNumber|string|false|none|none|
|idType|string|false|none|none|
|idNumber|string|false|none|none|
|localTaxNumber|string|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_ApiTransactionLine">ApiTransactionLine</h2>
<!-- backwards compatibility -->
<a id="schemaapitransactionline"></a>
<a id="schema_ApiTransactionLine"></a>
<a id="tocSapitransactionline"></a>
<a id="tocsapitransactionline"></a>

```json
{
  "currency": "string",
  "currency2": "string",
  "exchangeRate": 0,
  "vatCode": "string",
  "vatRate": "string",
  "itemDescription": "string",
  "itemClassification": "string",
  "taxableBasisCredit": 0,
  "taxableBasisDebet": 0,
  "valueVatCredit": 0,
  "valueVatDebet": 0,
  "totalValueLine": 0,
  "amountVatDeducted": 0,
  "taxableBasisCurrency2": 0,
  "valueVatCurrency2": 0,
  "totalValueLineCurrency2": 0,
  "countryDispatch": "string",
  "countryArrival": "string",
  "deliveryConditions": "string",
  "additionalDocumentReference": "string",
  "reportingType": "string",
  "transactionType": 0,
  "additionalTransactionType": 0,
  "intrastatCode": "string",
  "extrastatCode": "string",
  "additionalDescription": "string",
  "weight": 0,
  "unitOfMeasure": "string",
  "quantity": 0,
  "additionalUnitOfMeasure": "string",
  "commercialValue": 0,
  "statisticalValue": 0,
  "commercialValueCurrency2": 0,
  "statisticalValueCurrency2": 0,
  "itemType": "string",
  "modeOfTransport": 0,
  "regionDispatch": "string",
  "harbourDispatch": "string",
  "regionArrival": "string",
  "harbourArrival": "string",
  "countryOrigin": "string",
  "purchaseExtra1": "string",
  "purchaseExtra2": "string",
  "purchaseExtra3": "string",
  "purchaseExtra4": "string",
  "purchaseExtra5": "string",
  "purchaseExtra6": "string",
  "purchaseExtra7": "string",
  "purchaseExtra8": "string",
  "purchaseExtra9": "string",
  "purchaseExtra10": "string",
  "salesExtra1": "string",
  "salesExtra2": "string",
  "salesExtra3": "string",
  "salesExtra4": "string",
  "salesExtra5": "string",
  "salesExtra6": "string",
  "salesExtra7": "string",
  "salesExtra8": "string",
  "salesExtra9": "string",
  "salesExtra10": "string",
  "mossReporterVatNumberUsed": "string",
  "administrationCode": "string",
  "vatCodeAssignerCode": "string",
  "isOriginal": true,
  "deliveryConditionsPlace": "string",
  "regionOrigin": "string",
  "vatCodeAccountingKey": "string",
  "originalTaxRateApplied": "string",
  "originalVatcodeUsed": "string",
  "originalVatcodeUsedDescription": "string",
  "vatGlAccountCredit": "string",
  "vatGlAccountDebet": "string",
  "vatGlAccountPurchases": "string",
  "vatGlAccountSales": "string",
  "revenuesGlAccount": "string",
  "costsGlAccount": "string",
  "plantCode": "string",
  "materialTaxClassification": "string",
  "customerTaxClassification": "string",
  "invoiceLineNumber": "string",
  "unitPrice": 0,
  "creditNoteReason": "string",
  "generalLedgerId": "string",
  "generalLedgerType": "string",
  "journalDescription": "string",
  "journalId": "string",
  "journalType": "string",
  "statisticalProcedure": "string",
  "propertyCode": "string",
  "propertyRegisterReference": "string",
  "exemptReasonCode": "string",
  "utilizationDate": "2019-05-23T21:00:10Z",
  "annualProrate": 0,
  "annualDeduction": 0,
  "annualDeductionEffectiveDate": "2019-05-23T21:00:10Z",
  "assetId": "string",
  "deliveryIdentification": "string",
  "firstSemester": true,
  "withholdingAmount": 0,
  "operationType": "string",
  "profitCenter": "string",
  "discountBaseAmount": 0,
  "businessArea": "string",
  "costCenter": "string",
  "materialNumber": "string",
  "assignmentNumber": "string",
  "projectNumber": "string",
  "establishmentCode": "string",
  "creationDate": "2019-05-23T21:00:10Z",
  "creationTime": "string",
  "exchangeRate2": 0,
  "withholdingType": "string",
  "withholdingRate": 0,
  "withholdingDescription": "string",
  "salesOrderDate": "2019-05-23T21:00:10Z",
  "salesOrderNumber": "string",
  "purchaseOrderNumber": "string",
  "shipperCountryVATNumber": "string",
  "shipperCountryVATNumberUsed": "string",
  "shipperName": "string",
  "shipperLocalCode": "string",
  "shipmentType": "string",
  "shipmentDescription": "string",
  "shipmentWeightUOM": "string",
  "shipmentWeightGross": 0,
  "shipmentWeightNet": 0,
  "shipmentDateTime": "2019-05-23T21:00:10Z",
  "itemCodeType": "string",
  "itemCode": "string",
  "transactionEndDate": "2019-05-23T21:00:10Z",
  "paymentExpireDate": "2019-05-23T21:00:10Z",
  "paymentBankName": "string",
  "paymentCode": "string",
  "intBankAccountNumber": "string",
  "originalInvoiceDate": "2019-05-23T21:00:10Z",
  "shipmentNumofPackages": 0,
  "paymentDueDate": 0,
  "vatDueDate": "string",
  "virtualStamp": "string",
  "stampAmount": 0,
  "reaOffice": "string",
  "reaNumber": "string",
  "socialCapital": 0,
  "soleShareholder": "string",
  "statusLiquidation": "string",
  "referenceProvision": "string",
  "doacupCode": "string",
  "doacigCode": "string",
  "dtCtrDocumentID": "string",
  "dtCtrDate": "2019-05-23T21:00:10Z",
  "dtCtrItemNum": "string",
  "dtCtrConvCode": "string",
  "dtCtrCUPCode": "string",
  "dtCtrCIGCode": "string",
  "dtCnvDocumentID": "string",
  "dtCnvDate": "2019-05-23T21:00:10Z",
  "dtCnvItemNum": "string",
  "dtCnvConvCode": "string",
  "dtCnvCUPCode": "string",
  "dtCnvCIGCode": "string",
  "dtRczDocumentID": "string",
  "dtRczDate": "2019-05-23T21:00:10Z",
  "dtRczItemNum": "string",
  "dtRczConvCode": "string",
  "dtRczCUPCode": "string",
  "dtRczCIGCode": "string",
  "adGestionaliType": "string",
  "adGestionaliText": "string",
  "adGestionaliNumber": 0,
  "adGestionaliDate": "2019-05-23T21:00:10Z",
  "adGestionaliType2": "string",
  "adGestionaliText2": "string",
  "adGestionaliType3": "string",
  "adGestionaliText3": "string",
  "adGestionaliType4": "string",
  "adGestionaliText4": "string",
  "adGestionaliType5": "string",
  "adGestionaliText5": "string",
  "lineNature": "string",
  "lineAdminReference": "string",
  "shipmentCause": "string",
  "shipTimeStamp": "2019-05-23T21:00:10Z",
  "shipmentStartDate": "2019-05-23T21:00:10Z",
  "alboProfessional": "string",
  "alboProvince": "string",
  "alboInscriptionDate": "2019-05-23T21:00:10Z",
  "supplierLocalOfficeAddress": "string",
  "supplierLocalOfficeStreetNumber": "string",
  "supplierLocalOfficePostalCode": 0,
  "supplierLocalOfficeCity": "string",
  "supplierLocalOfficeProvince": "string",
  "supplierLocalOfficeCountry": "string",
  "supplierFiscalRepName": "string",
  "supplierFiscalRepTIN": "string",
  "supplierFiscalRepFirstName": "string",
  "supplierFiscalRepLastName": "string",
  "supplierFiscalRepCodEORI": "string",
  "customerLocalOfficeAddress": "string",
  "customerLocalOfficeStreetNumber": "string",
  "customerLocalOfficePostalCode": 0,
  "customerLocalOfficeCity": "string",
  "customerLocalOfficeProvince": "string",
  "customerLocalOfficeCountry": "string",
  "customerFiscalRepFirstName": "string",
  "customerFiscalRepLastName": "string",
  "roundingAmount": 0,
  "socSecType": "string",
  "socSecRate": 0,
  "socSecContributionAmount": 0,
  "socSecTaxableAmount": 0,
  "socSecVATRate": 0,
  "socSecWithheld": "string",
  "socSecNatura": "string",
  "socSecAdminReference": "string",
  "art73": "string",
  "stageReference": 0,
  "shipperTIN": "string",
  "driverFirstName": "string",
  "driverLastName": "string",
  "resaType": "string",
  "mainInvoiceNumber": "string",
  "mainInvoiceDate": "2019-05-23T21:00:10Z",
  "subjectWithheld": "string",
  "additionalExpenses": 0,
  "paymentRoundingAmount": 0,
  "vehicleRegistrationDate": "2019-05-23T21:00:10Z",
  "vehicleTotalTravel": "string",
  "paymentBeneficiary": "string",
  "officePostalCode": "string",
  "signerLastName": "string",
  "signerFirstName": "string",
  "signerTIN": "string",
  "abiCode": 0,
  "cabCode": 0,
  "prepaymentDiscount": 0,
  "prepaymentDueDate": "2019-05-23T21:00:10Z",
  "penaltyLatePayment": 0,
  "penaltyStartDate": "2019-05-23T21:00:10Z",
  "supplierFiscalRepTitle": "string",
  "driverTitle": "string",
  "doaNumItem": "string",
  "supplierFiscalRepCountryVATNumber": "string",
  "customerFiscalRepCountryVATNumber": "string",
  "salesOrderNumber2": "string",
  "salesOrderNumber3": "string",
  "salesOrderNumber4": "string",
  "salesOrderNumber5": "string"
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|currency|string|false|none|none|
|currency2|string|false|none|none|
|exchangeRate|number(double)|false|none|none|
|vatCode|string|false|none|none|
|vatRate|string|false|none|none|
|itemDescription|string|false|none|none|
|itemClassification|string|false|none|none|
|taxableBasisCredit|number(double)|false|none|none|
|taxableBasisDebet|number(double)|false|none|none|
|valueVatCredit|number(double)|false|none|none|
|valueVatDebet|number(double)|false|none|none|
|totalValueLine|number(double)|false|none|none|
|amountVatDeducted|number(double)|false|none|none|
|taxableBasisCurrency2|number(double)|false|none|none|
|valueVatCurrency2|number(double)|false|none|none|
|totalValueLineCurrency2|number(double)|false|none|none|
|countryDispatch|string|false|none|none|
|countryArrival|string|false|none|none|
|deliveryConditions|string|false|none|none|
|additionalDocumentReference|string|false|none|none|
|reportingType|string|false|none|none|
|transactionType|integer(int32)|false|none|none|
|additionalTransactionType|integer(int32)|false|none|none|
|intrastatCode|string|false|none|none|
|extrastatCode|string|false|none|none|
|additionalDescription|string|false|none|none|
|weight|number(double)|false|none|none|
|unitOfMeasure|string|false|none|none|
|quantity|number(double)|false|none|none|
|additionalUnitOfMeasure|string|false|none|none|
|commercialValue|number(double)|false|none|none|
|statisticalValue|number(double)|false|none|none|
|commercialValueCurrency2|number(double)|false|none|none|
|statisticalValueCurrency2|number(double)|false|none|none|
|itemType|string|false|none|none|
|modeOfTransport|integer(int32)|false|none|none|
|regionDispatch|string|false|none|none|
|harbourDispatch|string|false|none|none|
|regionArrival|string|false|none|none|
|harbourArrival|string|false|none|none|
|countryOrigin|string|false|none|none|
|purchaseExtra1|string|false|none|none|
|purchaseExtra2|string|false|none|none|
|purchaseExtra3|string|false|none|none|
|purchaseExtra4|string|false|none|none|
|purchaseExtra5|string|false|none|none|
|purchaseExtra6|string|false|none|none|
|purchaseExtra7|string|false|none|none|
|purchaseExtra8|string|false|none|none|
|purchaseExtra9|string|false|none|none|
|purchaseExtra10|string|false|none|none|
|salesExtra1|string|false|none|none|
|salesExtra2|string|false|none|none|
|salesExtra3|string|false|none|none|
|salesExtra4|string|false|none|none|
|salesExtra5|string|false|none|none|
|salesExtra6|string|false|none|none|
|salesExtra7|string|false|none|none|
|salesExtra8|string|false|none|none|
|salesExtra9|string|false|none|none|
|salesExtra10|string|false|none|none|
|mossReporterVatNumberUsed|string|false|none|none|
|administrationCode|string|false|none|none|
|vatCodeAssignerCode|string|false|none|none|
|isOriginal|boolean|false|none|none|
|deliveryConditionsPlace|string|false|none|none|
|regionOrigin|string|false|none|none|
|vatCodeAccountingKey|string|false|none|none|
|originalTaxRateApplied|string|false|none|none|
|originalVatcodeUsed|string|false|none|none|
|originalVatcodeUsedDescription|string|false|none|none|
|vatGlAccountCredit|string|false|none|none|
|vatGlAccountDebet|string|false|none|none|
|vatGlAccountPurchases|string|false|none|none|
|vatGlAccountSales|string|false|none|none|
|revenuesGlAccount|string|false|none|none|
|costsGlAccount|string|false|none|none|
|plantCode|string|false|none|none|
|materialTaxClassification|string|false|none|none|
|customerTaxClassification|string|false|none|none|
|invoiceLineNumber|string|false|none|none|
|unitPrice|number(double)|false|none|none|
|creditNoteReason|string|false|none|none|
|generalLedgerId|string|false|none|none|
|generalLedgerType|string|false|none|none|
|journalDescription|string|false|none|none|
|journalId|string|false|none|none|
|journalType|string|false|none|none|
|statisticalProcedure|string|false|none|none|
|propertyCode|string|false|none|none|
|propertyRegisterReference|string|false|none|none|
|exemptReasonCode|string|false|none|none|
|utilizationDate|string(date-time)|false|none|none|
|annualProrate|number(double)|false|none|none|
|annualDeduction|number(double)|false|none|none|
|annualDeductionEffectiveDate|string(date-time)|false|none|none|
|assetId|string|false|none|none|
|deliveryIdentification|string|false|none|none|
|firstSemester|boolean|false|none|none|
|withholdingAmount|number(double)|false|none|none|
|operationType|string|false|none|none|
|profitCenter|string|false|none|none|
|discountBaseAmount|number(double)|false|none|none|
|businessArea|string|false|none|none|
|costCenter|string|false|none|none|
|materialNumber|string|false|none|none|
|assignmentNumber|string|false|none|none|
|projectNumber|string|false|none|none|
|establishmentCode|string|false|none|none|
|creationDate|string(date-time)|false|none|none|
|creationTime|string|false|none|none|
|exchangeRate2|number(double)|false|none|none|
|withholdingType|string|false|none|none|
|withholdingRate|number(double)|false|none|none|
|withholdingDescription|string|false|none|none|
|salesOrderDate|string(date-time)|false|none|none|
|salesOrderNumber|string|false|none|none|
|purchaseOrderNumber|string|false|none|none|
|shipperCountryVATNumber|string|false|none|none|
|shipperCountryVATNumberUsed|string|false|none|none|
|shipperName|string|false|none|none|
|shipperLocalCode|string|false|none|none|
|shipmentType|string|false|none|none|
|shipmentDescription|string|false|none|none|
|shipmentWeightUOM|string|false|none|none|
|shipmentWeightGross|number(double)|false|none|none|
|shipmentWeightNet|number(double)|false|none|none|
|shipmentDateTime|string(date-time)|false|none|none|
|itemCodeType|string|false|none|none|
|itemCode|string|false|none|none|
|transactionEndDate|string(date-time)|false|none|none|
|paymentExpireDate|string(date-time)|false|none|none|
|paymentBankName|string|false|none|none|
|paymentCode|string|false|none|none|
|intBankAccountNumber|string|false|none|none|
|originalInvoiceDate|string(date-time)|false|none|none|
|shipmentNumofPackages|integer(int32)|false|none|none|
|paymentDueDate|integer(int32)|false|none|none|
|vatDueDate|string|false|none|none|
|virtualStamp|string|false|none|none|
|stampAmount|number(double)|false|none|none|
|reaOffice|string|false|none|none|
|reaNumber|string|false|none|none|
|socialCapital|number(double)|false|none|none|
|soleShareholder|string|false|none|none|
|statusLiquidation|string|false|none|none|
|referenceProvision|string|false|none|none|
|doacupCode|string|false|none|none|
|doacigCode|string|false|none|none|
|dtCtrDocumentID|string|false|none|none|
|dtCtrDate|string(date-time)|false|none|none|
|dtCtrItemNum|string|false|none|none|
|dtCtrConvCode|string|false|none|none|
|dtCtrCUPCode|string|false|none|none|
|dtCtrCIGCode|string|false|none|none|
|dtCnvDocumentID|string|false|none|none|
|dtCnvDate|string(date-time)|false|none|none|
|dtCnvItemNum|string|false|none|none|
|dtCnvConvCode|string|false|none|none|
|dtCnvCUPCode|string|false|none|none|
|dtCnvCIGCode|string|false|none|none|
|dtRczDocumentID|string|false|none|none|
|dtRczDate|string(date-time)|false|none|none|
|dtRczItemNum|string|false|none|none|
|dtRczConvCode|string|false|none|none|
|dtRczCUPCode|string|false|none|none|
|dtRczCIGCode|string|false|none|none|
|adGestionaliType|string|false|none|none|
|adGestionaliText|string|false|none|none|
|adGestionaliNumber|number(double)|false|none|none|
|adGestionaliDate|string(date-time)|false|none|none|
|adGestionaliType2|string|false|none|none|
|adGestionaliText2|string|false|none|none|
|adGestionaliType3|string|false|none|none|
|adGestionaliText3|string|false|none|none|
|adGestionaliType4|string|false|none|none|
|adGestionaliText4|string|false|none|none|
|adGestionaliType5|string|false|none|none|
|adGestionaliText5|string|false|none|none|
|lineNature|string|false|none|none|
|lineAdminReference|string|false|none|none|
|shipmentCause|string|false|none|none|
|shipTimeStamp|string(date-time)|false|none|none|
|shipmentStartDate|string(date-time)|false|none|none|
|alboProfessional|string|false|none|none|
|alboProvince|string|false|none|none|
|alboInscriptionDate|string(date-time)|false|none|none|
|supplierLocalOfficeAddress|string|false|none|none|
|supplierLocalOfficeStreetNumber|string|false|none|none|
|supplierLocalOfficePostalCode|integer(int32)|false|none|none|
|supplierLocalOfficeCity|string|false|none|none|
|supplierLocalOfficeProvince|string|false|none|none|
|supplierLocalOfficeCountry|string|false|none|none|
|supplierFiscalRepName|string|false|none|none|
|supplierFiscalRepTIN|string|false|none|none|
|supplierFiscalRepFirstName|string|false|none|none|
|supplierFiscalRepLastName|string|false|none|none|
|supplierFiscalRepCodEORI|string|false|none|none|
|customerLocalOfficeAddress|string|false|none|none|
|customerLocalOfficeStreetNumber|string|false|none|none|
|customerLocalOfficePostalCode|integer(int32)|false|none|none|
|customerLocalOfficeCity|string|false|none|none|
|customerLocalOfficeProvince|string|false|none|none|
|customerLocalOfficeCountry|string|false|none|none|
|customerFiscalRepFirstName|string|false|none|none|
|customerFiscalRepLastName|string|false|none|none|
|roundingAmount|number(double)|false|none|none|
|socSecType|string|false|none|none|
|socSecRate|number(double)|false|none|none|
|socSecContributionAmount|number(double)|false|none|none|
|socSecTaxableAmount|number(double)|false|none|none|
|socSecVATRate|number(double)|false|none|none|
|socSecWithheld|string|false|none|none|
|socSecNatura|string|false|none|none|
|socSecAdminReference|string|false|none|none|
|art73|string|false|none|none|
|stageReference|integer(int32)|false|none|none|
|shipperTIN|string|false|none|none|
|driverFirstName|string|false|none|none|
|driverLastName|string|false|none|none|
|resaType|string|false|none|none|
|mainInvoiceNumber|string|false|none|none|
|mainInvoiceDate|string(date-time)|false|none|none|
|subjectWithheld|string|false|none|none|
|additionalExpenses|number(double)|false|none|none|
|paymentRoundingAmount|number(double)|false|none|none|
|vehicleRegistrationDate|string(date-time)|false|none|none|
|vehicleTotalTravel|string|false|none|none|
|paymentBeneficiary|string|false|none|none|
|officePostalCode|string|false|none|none|
|signerLastName|string|false|none|none|
|signerFirstName|string|false|none|none|
|signerTIN|string|false|none|none|
|abiCode|integer(int32)|false|none|none|
|cabCode|integer(int32)|false|none|none|
|prepaymentDiscount|number(double)|false|none|none|
|prepaymentDueDate|string(date-time)|false|none|none|
|penaltyLatePayment|number(double)|false|none|none|
|penaltyStartDate|string(date-time)|false|none|none|
|supplierFiscalRepTitle|string|false|none|none|
|driverTitle|string|false|none|none|
|doaNumItem|string|false|none|none|
|supplierFiscalRepCountryVATNumber|string|false|none|none|
|customerFiscalRepCountryVATNumber|string|false|none|none|
|salesOrderNumber2|string|false|none|none|
|salesOrderNumber3|string|false|none|none|
|salesOrderNumber4|string|false|none|none|
|salesOrderNumber5|string|false|none|none|

</section>
</section>

<section>
<h2 id="tocS_EntitySpaceTransactionRequest">EntitySpaceTransactionRequest</h2>
<!-- backwards compatibility -->
<a id="schemaentityspacetransactionrequest"></a>
<a id="schema_EntitySpaceTransactionRequest"></a>
<a id="tocSentityspacetransactionrequest"></a>
<a id="tocsentityspacetransactionrequest"></a>

```json
{
  "entities": [
    {
      "name": "string",
      "fields": [
        {
          "name": "string",
          "value": {}
        }
      ],
      "entities": [
        null
      ]
    }
  ],
  "data": "string",
  "erpSystemId": "string",
  "actionsOverride": [
    "string"
  ],
  "importProfileName": "string",
  "messages": [
    {
      "status": 0,
      "category": "string",
      "code": "string",
      "description": "string",
      "legalStatusComments": "string",
      "legalTrackingId": "string",
      "processStartedTimestamp": "2019-05-23T21:00:10Z",
      "sendToErp": true
    }
  ],
  "attachments": [
    {
      "name": "string",
      "type": "string",
      "link": "string",
      "content": "string"
    }
  ]
}

```

<section>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|entities|[[TransmissionServiceEntity](#schematransmissionserviceentity)]|false|none|none|
|data|string|false|none|none|
|erpSystemId|string|false|none|none|
|actionsOverride|[string]|false|none|none|
|importProfileName|string|false|none|none|
|messages|[[TransmissionMessage](#schematransmissionmessage)]|false|none|none|
|attachments|[[TransmissionAttachment](#schematransmissionattachment)]|false|none|none|

</section>
</section>

