# NetLicensing: Get Token

Retrieves a token from NetLicensing.

```
GET https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/get-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/get-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/get-token?${params}`, {
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
      "licenseeNumber": "string",
      "lists": {},
      "number": "string",
      "shopURL": "https://example.com",
      "tokenType": "string",
      "type": "string",
      "vendorNumber": "string"
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
| `licenseeNumber` | string |  |
| `lists` | object |  |
| `number` | string |  |
| `shopURL` | string |  |
| `tokenType` | string |  |
| `type` | string |  |
| `vendorNumber` | string |  |

## Native endpoint

Through the native NetLicensing API, this operation is `GET /token/{tokenNumber}` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token.md) for the provider-specific parameters and requirements.

