# Evoliz: Create Client

Creates a new client in Evoliz.

```
POST https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client', {
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
      "address": {
        "country": {
          "iso2": "string",
          "label": "string"
        },
        "postcode": "string",
        "town": "string"
      },
      "clientid": 1,
      "code": "string",
      "comment": "string",
      "enabled": true,
      "name": "Ava Chen",
      "phone": "string",
      "safe_amount": 1,
      "stampdate": "2026-05-07T12:00:00.000Z",
      "ttc": true,
      "type": "string",
      "userid": 1,
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.country.iso2` | string |  |
| `address.country.label` | string |  |
| `address.postcode` | string |  |
| `address.town` | string |  |
| `clientid` | number |  |
| `code` | string |  |
| `comment` | string |  |
| `enabled` | boolean |  |
| `name` | string |  |
| `phone` | string |  |
| `safe_amount` | number |  |
| `stampdate` | date |  |
| `ttc` | boolean |  |
| `type` | string |  |
| `userid` | number |  |
| `vat_number` | string |  |

## Native endpoint

Through the native Evoliz API, this operation is `POST /api/v1/clients` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

