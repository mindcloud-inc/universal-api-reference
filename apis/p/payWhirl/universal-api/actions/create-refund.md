# PayWhirl: Create Refund

Creates a refund for a PayWhirl charge.

```
POST https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chargeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/create-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chargeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chargeId` | number | yes | The PayWhirl charge ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "billFee": 1,
      "createdAt": "string",
      "currency": "string",
      "customerId": 1,
      "deletedAt": "string",
      "description": "string",
      "fee": 1,
      "gatewayId": 1,
      "gatewayReference": "string",
      "id": 1,
      "refunded": 1,
      "refundedAmount": 1,
      "refundedOn": 1,
      "refundReference": "string",
      "updatedAt": "string",
      "usd": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `billFee` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customerId` | number |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `fee` | number |  |
| `gatewayId` | number |  |
| `gatewayReference` | string |  |
| `id` | number |  |
| `refunded` | number |  |
| `refundedAmount` | number |  |
| `refundedOn` | number |  |
| `refundReference` | string |  |
| `updatedAt` | string |  |
| `usd` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `POST /refund/charge/{id}` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refund.md) for the provider-specific parameters and requirements.

