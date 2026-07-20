# NetLicensing: Create Token

Creates a new token in NetLicensing.

```
POST https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native NetLicensing API, this operation is `POST /token` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-token.md) for the provider-specific parameters and requirements.

