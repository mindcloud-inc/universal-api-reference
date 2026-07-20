# Turis: Create Delivery

Creates a new delivery in Turis.

```
POST https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-delivery', {
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
      "address": "string",
      "city": "string",
      "companyId": 1,
      "companyName": "Ava Chen",
      "country": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "locationName": "Ava Chen",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `companyId` | number |  |
| `companyName` | string |  |
| `country` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `locationName` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Turis API, this operation is `POST /api/public/v1/deliveries` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-delivery.md) for the provider-specific parameters and requirements.

