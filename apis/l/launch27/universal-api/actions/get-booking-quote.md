# Launch27: Get Booking Quote

Retrieves a booking quote from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-booking-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-booking-quote?connectionId=$CONNECTION_ID&quote_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "quote_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-booking-quote?${params}`, {
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
| `quote_uuid` | string | yes | Launch27 quote UUID used to retrieve a booking quote. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "arrival_window": 1,
      "city": "string",
      "custom_fields": [
        {}
      ],
      "customer_notes": "string",
      "discount_code": "string",
      "email": "ava@example.com",
      "final_price": 1,
      "first_name": "Ava",
      "frequency_id": 1,
      "last_name": "Chen",
      "location_id": 1,
      "payment_method": "string",
      "phone": "string",
      "service_date": "string",
      "services": [
        {}
      ],
      "sms_notifications": true,
      "state": "string",
      "tip": 1,
      "tip_recurring": 1,
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Customer address from the booking quote. |
| `arrival_window` | number | Arrival window selected for the quoted booking. |
| `city` | string | Customer city from the booking quote. |
| `custom_fields` | array<object> | Quoted custom field values to reuse when turning the quote into a booking. |
| `customer_notes` | string | Customer notes captured on the quote. |
| `discount_code` | string | Discount code carried by the quote. |
| `email` | string | Customer email from the booking quote. |
| `final_price` | number | Final quoted booking price used to populate the booking summary. |
| `first_name` | string | Customer first name from the booking quote. |
| `frequency_id` | number | Launch27 frequency ID referenced by the booking quote. |
| `last_name` | string | Customer last name from the booking quote. |
| `location_id` | number | Launch27 location ID referenced by the booking quote. |
| `payment_method` | string | Payment method code stored on the quote. |
| `phone` | string | Customer phone number from the booking quote. |
| `service_date` | string | Quoted service date/time used to prefill booking scheduling. |
| `services` | array<object> | Quoted service selections, including pricing parameters and extras. |
| `sms_notifications` | boolean | Whether SMS notifications are enabled on the quote. |
| `state` | string | Customer state from the booking quote. |
| `tip` | number | One-time tip amount stored on the quote. |
| `tip_recurring` | number | Recurring tip amount stored on the quote. |
| `zip` | string | Customer postal code from the booking quote. |

## Native endpoint

Through the native Launch27 API, this operation is `POST booking/quote` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-quote.md) for the provider-specific parameters and requirements.

