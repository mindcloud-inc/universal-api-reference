# Payfunnels: Pause Subscription

Updates a subscription by pausing it in Payfunnels.

```
PUT https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/pause-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/pause-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "behavior": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/pause-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "behavior": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `behavior` | string | yes | How the paused subscription behaves. |
| `chargeUnpaidInvoice` | boolean | no | Charge unpaid invoices when resuming from a temporary pause. |
| `id` | string | yes | Subscription ID. |
| `resumeAt` | number | no | UNIX timestamp to resume automatically. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "chargeAmount": 1,
      "createdAt": "string",
      "customer": {},
      "endDate": "string",
      "id": "string",
      "metadata": {},
      "paymentMethod": {},
      "paymentType": "string",
      "startDate": "string",
      "status": "string",
      "title": "string",
      "totalCollectedAmount": 1,
      "totalDueAmount": 1,
      "totalMaxPayment": 1,
      "totalSubscriptionAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `chargeAmount` | number |  |
| `createdAt` | string |  |
| `customer` | object |  |
| `endDate` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `paymentMethod` | object |  |
| `paymentType` | string |  |
| `startDate` | string |  |
| `status` | string |  |
| `title` | string |  |
| `totalCollectedAmount` | number |  |
| `totalDueAmount` | number |  |
| `totalMaxPayment` | number |  |
| `totalSubscriptionAmount` | number |  |

## Native endpoint

Through the native Payfunnels API, this operation is `POST /v1/subscriptions/pause` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-subscription.md) for the provider-specific parameters and requirements.

