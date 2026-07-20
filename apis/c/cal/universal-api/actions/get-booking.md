# Cal.com: Get Booking

Retrieves a booking from Cal.com.

```
GET https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-booking?connectionId=$CONNECTION_ID&bookingUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-booking?${params}`, {
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
| `bookingUid` | list | yes | Booking identifier from Cal.com path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {}
      ],
      "createdAt": "string",
      "description": "string",
      "duration": 1,
      "end": "string",
      "eventTypeId": 1,
      "guests": [
        "string"
      ],
      "id": 1,
      "location": "string",
      "meetingUrl": "https://example.com",
      "metadata": {},
      "start": "string",
      "status": "string",
      "title": "string",
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `end` | string |  |
| `eventTypeId` | number |  |
| `guests` | array<string> |  |
| `id` | number |  |
| `location` | string |  |
| `meetingUrl` | string |  |
| `metadata` | object |  |
| `start` | string |  |
| `status` | string |  |
| `title` | string |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `GET /bookings/:bookingUid` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

