# Beds24: List Booking Invoices

Retrieves booking invoices from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-booking-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-booking-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-booking-invoices?${params}`, {
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
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "invoiceId": 1,
      "invoiceItems": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiceDate` | date |  |
| `invoiceId` | number |  |
| `invoiceItems` | array<object> |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /bookings/invoices` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-invoices.md) for the provider-specific parameters and requirements.

