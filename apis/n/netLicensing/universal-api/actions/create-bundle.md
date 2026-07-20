# NetLicensing: Create Bundle

Creates a new bundle in NetLicensing.

```
POST https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-bundle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-bundle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-bundle', {
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
      "currency": "string",
      "description": "string",
      "licenseTemplatesNumbers": "string",
      "lists": {},
      "name": "Ava Chen",
      "number": "string",
      "price": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `licenseTemplatesNumbers` | string |  |
| `lists` | object |  |
| `name` | string |  |
| `number` | string |  |
| `price` | string |  |
| `type` | string |  |

## Native endpoint

Through the native NetLicensing API, this operation is `POST /bundle` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bundle.md) for the provider-specific parameters and requirements.

