# Mighty Networks: List Events

Retrieves events from a Mighty Networks network.

```
GET https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0&networkId=%7B%7Bcredentials.networkId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "networkId": "{{credentials.networkId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-events?${params}`, {
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
| `networkId` | string | yes | The Mighty Networks network ID or subdomain for the request path. Default: `{{credentials.networkId}}`. |

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

Through the native Mighty Networks API, this operation is `GET /networks/:network_id/events` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

