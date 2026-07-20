# Flexopus: Create Event

Creates a new event in Flexopus.

```
POST https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toTime": "2026-05-07T12:00:00.000Z",
  "name": "Ava Chen",
  "organizerUserId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toTime": "2026-05-07T12:00:00.000Z",
    "name": "Ava Chen",
    "organizerUserId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromTime` | date | no | When the event will start. |
| `fromTimezone` | string | no | Display timezone of the event start time. |
| `toTime` | date | yes | When the event will end. |
| `toTimezone` | string | no | Display timezone of the event end time. |
| `classification` | list<number> | no | Access classification for the event. One of: `0`, `1`, `2`, `3`. |
| `name` | string | yes | Event name. |
| `description` | string | no | Event markdown description. |
| `organizerUserId` | number | yes | ID of the event organizer user. |
| `attendees[]` | array<object> | no | List of attendees for the event as a JSON array of attendee objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attendees": [
          {
            "email": "ava@example.com",
            "id": 1,
            "name": "Ava Chen",
            "role": 1,
            "status": 1
          }
        ],
        "bookables": [
          {
            "capacity": 1,
            "id": 1,
            "integration_email": "ava@example.com",
            "name": "Ava Chen",
            "tags": [
              "string"
            ]
          }
        ],
        "classification": 1,
        "from": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen",
        "organizer": {
          "name": "Ava Chen"
        },
        "status": 1,
        "to": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.attendees` | array<object> |  |
| `data.attendees[].email` | string |  |
| `data.attendees[].id` | number |  |
| `data.attendees[].name` | string |  |
| `data.attendees[].role` | number |  |
| `data.attendees[].status` | number |  |
| `data.bookables` | array<object> |  |
| `data.bookables[].capacity` | number |  |
| `data.bookables[].id` | number |  |
| `data.bookables[].integration_email` | string |  |
| `data.bookables[].name` | string |  |
| `data.bookables[].tags` | array<string> |  |
| `data.classification` | number |  |
| `data.from` | date |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.organizer` | object |  |
| `data.organizer.name` | string |  |
| `data.status` | number |  |
| `data.to` | date |  |

## Native endpoint

Through the native Flexopus API, this operation is `POST /events` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

