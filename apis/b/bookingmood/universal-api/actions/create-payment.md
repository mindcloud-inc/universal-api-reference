# Bookingmood: Create Payment

Creates a new payment in the Bookingmood API.

```
POST https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/create-payment', {
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
      "amount": 1,
      "booking_id": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "due_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invoice_id": "string",
      "notification_sent_at": "2026-05-07T12:00:00.000Z",
      "offline": true,
      "paid": 1,
      "provider_id": "string",
      "reference": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `booking_id` | string |  |
| `completed_at` | date |  |
| `created_at` | date |  |
| `currency` | string |  |
| `due_at` | date |  |
| `id` | string |  |
| `invoice_id` | string |  |
| `notification_sent_at` | date |  |
| `offline` | boolean |  |
| `paid` | number |  |
| `provider_id` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Bookingmood API, this operation is `POST /payments` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

