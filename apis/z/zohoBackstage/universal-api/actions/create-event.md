# Zoho Backstage: Create Event



```
POST https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "name": "Ava Chen",
  "timezone": "string",
  "startTime": "string",
  "endTime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "name": "Ava Chen",
    "timezone": "string",
    "startTime": "string",
    "endTime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | string | yes | The Zoho Backstage portal ID. |
| `name` | string | yes | The event name. |
| `timezone` | string | yes | The event timezone. |
| `startTime` | string | yes | The event start time in UTC ISO 8601 format. |
| `endTime` | string | yes | The event end time in UTC ISO 8601 format. |
| `language` | string | no | The event language code. |
| `eventType` | number | no | The numeric event type: 2 venue, 3 online, 4 hybrid. |
| `summary` | string | no | A short summary of the event. |
| `description` | string | no | The event description. |
| `category` | string | no | The event category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "created_time": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "end_time": "2026-05-07T12:00:00.000Z",
      "event_type": 1,
      "event_type_string": "string",
      "id": "string",
      "language": "string",
      "last_modified_time": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "start_time": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "status_string": "string",
      "summary": "string",
      "thumbnail_url": "https://example.com",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `created_time` | date |  |
| `description` | string |  |
| `end_time` | date |  |
| `event_type` | number |  |
| `event_type_string` | string |  |
| `id` | string |  |
| `language` | string |  |
| `last_modified_time` | date |  |
| `name` | string |  |
| `start_time` | date |  |
| `status` | number |  |
| `status_string` | string |  |
| `summary` | string |  |
| `thumbnail_url` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `POST /v3/portals/:portal_id/events` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

