# NetLicensing: List Products

Finds products in NetLicensing by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "apiKeyRole": "string",
      "code": "string",
      "currency": "string",
      "isEu": "string",
      "licenseeNumber": "string",
      "licenseTemplateNumber": "string",
      "licenseType": "string",
      "licensingModel": "string",
      "lists": {},
      "name": "Ava Chen",
      "number": "string",
      "price": "string",
      "productNumber": "string",
      "shopURL": "https://example.com",
      "source": "string",
      "status": "string",
      "tokenType": "string",
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `apiKeyRole` | string |  |
| `code` | string |  |
| `currency` | string |  |
| `isEu` | string |  |
| `licenseeNumber` | string |  |
| `licenseTemplateNumber` | string |  |
| `licenseType` | string |  |
| `licensingModel` | string |  |
| `lists` | object |  |
| `name` | string |  |
| `number` | string |  |
| `price` | string |  |
| `productNumber` | string |  |
| `shopURL` | string |  |
| `source` | string |  |
| `status` | string |  |
| `tokenType` | string |  |
| `type` | string |  |
| `version` | string |  |

## Native endpoint

Through the native NetLicensing API, this operation is `GET /product` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

