# Orufy Bookings: Create Booking



```
POST https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessLink": "https://example.com",
  "slug": "string",
  "timezone": "string",
  "time[]": [
    {}
  ],
  "answers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessLink": "https://example.com",
    "slug": "string",
    "timezone": "string",
    "time[]": [{}],
    "answers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessLink` | string | yes | The Orufy access link, for example `mindcloud`. |
| `slug` | string | yes | The public event slug, for example `30-min-intro-call`. |
| `timezone` | string | yes | An IANA timezone, for example `America/Sao_Paulo`. |
| `time[]` | array<object> | yes | An array of time objects. Each item must include a `time` ISO datetime value. |
| `answers[]` | array<object> | yes | An array of booking answers. Each item should include `name` and `answer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isSuccess": true,
      "queueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSuccess` | boolean |  |
| `queueId` | string |  |

## Native endpoint

Through the native Orufy Bookings API, this operation is `POST /meet/book` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

