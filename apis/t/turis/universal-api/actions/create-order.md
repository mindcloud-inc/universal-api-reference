# Turis: Create Order

Creates a new order in Turis.

```
POST https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-order', {
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
      "buyerComment": "string",
      "comment": "string",
      "deliveryAddress": {
        "address": "string",
        "companyName": "Ava Chen",
        "zipCode": "string"
      },
      "deliveryId": "string",
      "orderId": 1,
      "shippingPrice": 1,
      "userId": 1,
      "vatRatePreserved": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyerComment` | string |  |
| `comment` | string |  |
| `deliveryAddress.address` | string |  |
| `deliveryAddress.companyName` | string |  |
| `deliveryAddress.zipCode` | string |  |
| `deliveryId` | string |  |
| `orderId` | number |  |
| `shippingPrice` | number |  |
| `userId` | number |  |
| `vatRatePreserved` | number |  |

## Native endpoint

Through the native Turis API, this operation is `POST /api/public/v1/orders` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

