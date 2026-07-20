# Orufy Bookings: Validate Booking Slot



```
GET https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/validate-booking-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/validate-booking-slot?connectionId=$CONNECTION_ID&accessLink=https%3A%2F%2Fexample.com&slug=string&timezone=string&time%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessLink": "https://example.com",
  "slug": "string",
  "timezone": "string",
  "time[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/validate-booking-slot?${params}`, {
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
| `accessLink` | string | yes | The Orufy access link, for example `mindcloud`. |
| `slug` | string | yes | The public event slug, for example `30-min-intro-call`. |
| `timezone` | string | yes | An IANA timezone, for example `America/Sao_Paulo`. |
| `time[]` | array<object> | yes | An array of time objects. Each item must include a `time` ISO datetime value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSuccess` | boolean |  |

## Native endpoint

Through the native Orufy Bookings API, this operation is `POST /meet/slot/validate` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-booking-slot.md) for the provider-specific parameters and requirements.

