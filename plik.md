---
title: OpenAPI definition v0
language_tabs:
  - http: HTTP
  - shell: Shell
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="openapi-definition">OpenAPI definition v0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="http://localhost:9090">http://localhost:9090</a>

<h1 id="openapi-definition-wallet-controller">wallet-controller</h1>

## getAllWallets

<a id="opIdgetAllWallets"></a>

> Code samples

```http
GET http://localhost:9090/api/wallet HTTP/1.1
Host: localhost:9090
Accept: */*

```

```shell
# You can also use wget
curl -X GET http://localhost:9090/api/wallet \
  -H 'Accept: */*'

```

`GET /api/wallet`

> Example responses

> 200 Response

<h3 id="getallwallets-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|string|

<h3 id="getallwallets-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[WalletDTO](#schemawalletdto)]|false|none|none|
|» id|integer(int64)|false|none|none|
|» name|string|false|none|none|
|» creationDate|string(date-time)|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## createWallet

<a id="opIdcreateWallet"></a>

> Code samples

```http
POST http://localhost:9090/api/wallet HTTP/1.1
Host: localhost:9090
Content-Type: application/json
Accept: */*

```

```shell
# You can also use wget
curl -X POST http://localhost:9090/api/wallet \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'

```

`POST /api/wallet`

> Body parameter

```json
{
  "name": "string"
}
```

<h3 id="createwallet-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateWalletDTO](#schemacreatewalletdto)|true|none|

> Example responses

> 200 Response

<h3 id="createwallet-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[WalletDTO](#schemawalletdto)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|string|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_CreateWalletDTO">CreateWalletDTO</h2>
<!-- backwards compatibility -->
<a id="schemacreatewalletdto"></a>
<a id="schema_CreateWalletDTO"></a>
<a id="tocScreatewalletdto"></a>
<a id="tocscreatewalletdto"></a>

```json
{
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|

<h2 id="tocS_WalletDTO">WalletDTO</h2>
<!-- backwards compatibility -->
<a id="schemawalletdto"></a>
<a id="schema_WalletDTO"></a>
<a id="tocSwalletdto"></a>
<a id="tocswalletdto"></a>

```json
{
  "id": 0,
  "name": "string",
  "creationDate": "2019-08-24T14:15:22Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|name|string|false|none|none|
|creationDate|string(date-time)|false|none|none|

