# Evervault: Create Merchant

Creates a new merchant in Evervault.

```
POST https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-merchant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-merchant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-merchant', {
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
      "applePay": {},
      "business": {},
      "categoryCode": "string",
      "createdAt": 1,
      "id": "string",
      "name": "Ava Chen",
      "networkTokens": {},
      "updatedAt": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applePay` | object |  |
| `business` | object |  |
| `categoryCode` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `name` | string |  |
| `networkTokens` | object |  |
| `updatedAt` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Evervault API, this operation is `POST /payments/merchants` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-merchant.md) for the provider-specific parameters and requirements.

