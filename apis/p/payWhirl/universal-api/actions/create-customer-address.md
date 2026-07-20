# PayWhirl: Create Customer Address

Creates a new customer address in PayWhirl.

```
POST https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-customer-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-customer-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-customer-address', {
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
      "country": "string",
      "createdAt": "string",
      "customerId": 1,
      "deletedAt": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "metadata": "string",
      "phone": "string",
      "state": "string",
      "updatedAt": "string",
      "userId": 1,
      "zip": "string"
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
| `country` | string |  |
| `createdAt` | string |  |
| `customerId` | number |  |
| `deletedAt` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `metadata` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |
| `zip` | string |  |

## Native endpoint

Through the native PayWhirl API, this operation is `POST /customer/address` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-address.md) for the provider-specific parameters and requirements.

