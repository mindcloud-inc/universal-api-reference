# Understory: Get Booking

Retrieves a booking from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-booking?connectionId=$CONNECTION_ID&bookingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-booking?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingId` | string | yes | The unique identifier of the booking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer": {
        "address": {
          "address_lines": [
            [
              "string"
            ]
          ],
          "city": "string",
          "country": "string",
          "region": "string",
          "zip_code": "string"
        },
        "company_name": "Ava Chen",
        "customer_type": "string",
        "email": "ava@example.com",
        "full_name": "Ava Chen",
        "name": "Ava Chen",
        "phone": "string",
        "vat_number": "string"
      },
      "event_id": "string",
      "experience_id": "string",
      "id": "string",
      "internal_note": "string",
      "locale": "string",
      "source": "string",
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
| `company_id` | string |  |
| `created_at` | date |  |
| `customer.address.address_lines[]` | array<string> |  |
| `customer.address.city` | string |  |
| `customer.address.country` | string |  |
| `customer.address.region` | string |  |
| `customer.address.zip_code` | string |  |
| `customer.company_name` | string |  |
| `customer.customer_type` | string |  |
| `customer.email` | string |  |
| `customer.full_name` | string |  |
| `customer.name` | string |  |
| `customer.phone` | string |  |
| `customer.vat_number` | string |  |
| `event_id` | string |  |
| `experience_id` | string |  |
| `id` | string |  |
| `internal_note` | string |  |
| `locale` | string |  |
| `source` | string |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/bookings/{{bookingId}}` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

