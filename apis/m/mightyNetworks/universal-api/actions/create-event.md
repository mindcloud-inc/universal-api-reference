# Mighty Networks: Create Event

Creates a new event in Mighty Networks.

```
POST https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "networkId": "{{credentials.networkId}}",
  "spaceId": 1,
  "title": "string",
  "startsAt": "string",
  "endsAt": "string",
  "eventType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "networkId": "{{credentials.networkId}}",
    "spaceId": 1,
    "title": "string",
    "startsAt": "string",
    "endsAt": "string",
    "eventType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `networkId` | string | yes | The Mighty Networks network ID. Default: `{{credentials.networkId}}`. |
| `spaceId` | number | yes | The ID of the space that will host the event. |
| `title` | string | yes | The event title. |
| `startsAt` | string | yes | The event start time in ISO-8601 format. |
| `endsAt` | string | yes | The event end time in ISO-8601 format. |
| `eventType` | string | yes | The event type, such as online_meeting or local_meetup. |
| `description` | string | no | Optional event description. |
| `link` | string | no | Optional event link for online events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {
        "admin": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "shortBio": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "description": "string",
      "endsAt": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "frequency": "string",
      "id": 1,
      "images": [
        "string"
      ],
      "interval": 1,
      "link": "https://example.com",
      "location": "string",
      "permalink": "https://example.com",
      "postInFeed": true,
      "postType": "string",
      "recurrenceRule": "string",
      "restrictedEvent": true,
      "rsvpClosed": true,
      "rsvpEnabled": true,
      "startsAt": "2026-05-07T12:00:00.000Z",
      "timeZone": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `creator` | object |  |
| `creator.admin` | boolean |  |
| `creator.createdAt` | date |  |
| `creator.email` | string |  |
| `creator.id` | number |  |
| `creator.name` | string |  |
| `creator.shortBio` | string |  |
| `creator.updatedAt` | date |  |
| `description` | string |  |
| `endsAt` | date |  |
| `eventType` | string |  |
| `frequency` | string |  |
| `id` | number |  |
| `images` | array<string> |  |
| `interval` | number |  |
| `link` | string |  |
| `location` | string |  |
| `permalink` | string |  |
| `postInFeed` | boolean |  |
| `postType` | string |  |
| `recurrenceRule` | string |  |
| `restrictedEvent` | boolean |  |
| `rsvpClosed` | boolean |  |
| `rsvpEnabled` | boolean |  |
| `startsAt` | date |  |
| `timeZone` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `POST /networks/:network_id/events` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

