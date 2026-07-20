# TeamBook: Get Booking

Retrieves detailed booking information from TeamBook.

```
GET https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/get-booking?connectionId=$CONNECTION_ID&bookingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/get-booking?${params}`, {
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
| `bookingId` | string | yes | The TeamBook booking identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "id": "string",
      "location": 1,
      "order": "string",
      "project_id": "string",
      "tentative": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `created_at` | date |  |
| `date` | date |  |
| `duration` | string |  |
| `id` | string |  |
| `location` | number |  |
| `order` | string |  |
| `project_id` | string |  |
| `tentative` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native TeamBook API, this operation is `GET /bookings/{bookingId}` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

