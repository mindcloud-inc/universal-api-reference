# Bookingmood: List Payments

Retrieves payment records from the Bookingmood API.

```
GET https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-payments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Bookingmood API, this operation is `GET /payments` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

