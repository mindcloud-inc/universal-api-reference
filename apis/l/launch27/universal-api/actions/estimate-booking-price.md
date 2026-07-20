# Launch27: Estimate Booking Price

Retrieves a booking price estimate from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/estimate-booking-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/estimate-booking-price?connectionId=$CONNECTION_ID&location_id=1&frequency_id=1&service_date=string&services=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location_id": "1",
  "frequency_id": "1",
  "service_date": "string",
  "services": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/estimate-booking-price?${params}`, {
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
| `location_id` | number | yes | Launch27 location ID for the booking estimate. |
| `frequency_id` | number | yes | Launch27 booking frequency ID. |
| `service_date` | string | yes | Service date-time in Launch27 backend format YYYY-MM-DDTHH:mm:ss. |
| `services` | list<object> | yes | Array of selected Launch27 booking services. |
| `email` | string | no | Customer email for estimate validation and discount logic. |
| `tip` | number | no | Optional tip amount. |
| `discount_code` | string | no | Optional booking discount code. |
| `quote_uuid` | string | no | Optional Launch27 quote UUID to estimate from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discount_amount": 1,
      "discount_message": "string",
      "extras": 1,
      "giftcard_amount": 1,
      "price_adjustment": 1,
      "price_adjustment_after_tax": true,
      "price_for_discount_by_code": 1,
      "price_for_frequency": 1,
      "price_for_referral": 1,
      "price_recurring_for_frequency": 1,
      "services": 1,
      "tip": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discount_amount` | number |  |
| `discount_message` | string |  |
| `extras` | number |  |
| `giftcard_amount` | number |  |
| `price_adjustment` | number |  |
| `price_adjustment_after_tax` | boolean |  |
| `price_for_discount_by_code` | number |  |
| `price_for_frequency` | number |  |
| `price_for_referral` | number |  |
| `price_recurring_for_frequency` | number |  |
| `services` | number |  |
| `tip` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Launch27 API, this operation is `POST booking/estimate_price` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-booking-price.md) for the provider-specific parameters and requirements.

