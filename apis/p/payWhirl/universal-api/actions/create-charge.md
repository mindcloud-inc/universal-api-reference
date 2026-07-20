# PayWhirl: Create Charge

Creates a new charge in PayWhirl.

```
POST https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-charge', {
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
      "amountDue": 1,
      "cardId": 1,
      "chargeId": 1,
      "createdAt": "string",
      "currency": "string",
      "customerId": 1,
      "deletedAt": "string",
      "id": 1,
      "items": [
        {
          "amount": 1,
          "description": "string",
          "id": 1,
          "quantity": 1
        }
      ],
      "nextPaymentAttempt": 1,
      "paid": 1,
      "periodEnd": 1,
      "periodStart": 1,
      "promoCode": "string",
      "status": "string",
      "subscriptionId": 1,
      "subtotal": 1,
      "trackingNumber": "string",
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountDue` | number |  |
| `cardId` | number |  |
| `chargeId` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customerId` | number |  |
| `deletedAt` | string |  |
| `id` | number |  |
| `items[].amount` | number |  |
| `items[].description` | string |  |
| `items[].id` | number |  |
| `items[].quantity` | number |  |
| `nextPaymentAttempt` | number |  |
| `paid` | number |  |
| `periodEnd` | number |  |
| `periodStart` | number |  |
| `promoCode` | string |  |
| `status` | string |  |
| `subscriptionId` | number |  |
| `subtotal` | number |  |
| `trackingNumber` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `POST /create/charge` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-charge.md) for the provider-specific parameters and requirements.

