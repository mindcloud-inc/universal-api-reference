# Makeplans: Get Booking

Retrieves a booking from Makeplans.

```
GET https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-booking?connectionId=$CONNECTION_ID&bookingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-booking?${params}`, {
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
| `bookingId` | number | yes | The Makeplans booking ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "booked_from": "2026-05-07T12:00:00.000Z",
      "booked_to": "2026-05-07T12:00:00.000Z",
      "count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "notes": "string",
      "person_id": 1,
      "resource_id": 1,
      "service_id": 1,
      "state": "string",
      "status": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `booked_from` | date |  |
| `booked_to` | date |  |
| `count` | number |  |
| `created_at` | date |  |
| `id` | number |  |
| `notes` | string |  |
| `person_id` | number |  |
| `resource_id` | number |  |
| `service_id` | number |  |
| `state` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `GET /bookings/:bookingId` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

