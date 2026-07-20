# PayWhirl: Update Customer

Updates an existing customer in PayWhirl.

```
PUT https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/update-customer', {
  method: 'PUT',
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
      "currency": "string",
      "defaultCard": 1,
      "deletedAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "gatewayId": 1,
      "gatewayReference": "string",
      "gatewayType": "string",
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
| `currency` | string |  |
| `defaultCard` | number |  |
| `deletedAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `gatewayId` | number |  |
| `gatewayReference` | string |  |
| `gatewayType` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `metadata` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |
| `zip` | string |  |

## Native endpoint

Through the native PayWhirl API, this operation is `POST /update/customer` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

