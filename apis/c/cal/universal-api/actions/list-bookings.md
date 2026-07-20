# Cal.com: List Bookings

Retrieves bookings from Cal.com.

```
GET https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-bookings?${params}`, {
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
| `status` | list | no | Filter bookings by status. One of: `cancelled`, `past`, `recurring`, `rescheduled`, `unconfirmed`, `upcoming`. |
| `attendeeEmail` | string | no | Filter by attendee email. |
| `attendeeName` | string | no | Filter by attendee name. |
| `bookingUid` | list | no | Filter by booking UID. |
| `eventTypeId` | list | no | Filter by one event type ID. |
| `eventTypeIds` | string | no | Comma-separated event type IDs. |
| `teamId` | string | no | Filter by one team ID. |
| `teamsIds` | string | no | Comma-separated team IDs. |
| `afterStart` | string | no | Filter bookings with start after this ISO datetime. |
| `beforeEnd` | string | no | Filter bookings with end before this ISO datetime. |
| `afterCreatedAt` | string | no | Filter bookings created after this ISO datetime. |
| `beforeCreatedAt` | string | no | Filter bookings created before this ISO datetime. |
| `afterUpdatedAt` | string | no | Filter bookings updated after this ISO datetime. |
| `beforeUpdatedAt` | string | no | Filter bookings updated before this ISO datetime. |
| `sortStart` | list | no | Sort by start time (`asc` or `desc`). One of: `asc`, `desc`. |
| `sortEnd` | list | no | Sort by end time (`asc` or `desc`). One of: `asc`, `desc`. |
| `sortCreated` | list | no | Sort by creation time (`asc` or `desc`). One of: `asc`, `desc`. |
| `sortUpdatedAt` | list | no | Sort by update time (`asc` or `desc`). One of: `asc`, `desc`. |
| `take` | number | no | Number of bookings to return. |
| `skip` | number | no | Number of bookings to skip. |

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

Through the native Cal.com API, this operation is `GET /bookings` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

