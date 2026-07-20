# Zoho Backstage: Create Session



```
POST https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "eventId": "string",
  "title": "string",
  "track": "string",
  "sessionType": "string",
  "startTime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "eventId": "string",
    "title": "string",
    "track": "string",
    "sessionType": "string",
    "startTime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | string | yes | The Zoho Backstage portal ID. |
| `eventId` | string | yes | The Zoho Backstage event ID. |
| `title` | string | yes |  |
| `track` | string | yes |  |
| `sessionType` | string | yes |  |
| `startTime` | string | yes |  |
| `duration` | number | no |  |
| `venue` | string | no |  |
| `featured` | boolean | no |  |
| `venueToBeAnnounced` | boolean | no |  |
| `hidden` | boolean | no |  |
| `speakers[]` | array<string> | no |  |
| `timeToBeAnnounced` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenda": "string",
      "created_time": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "featured": true,
      "hidden": true,
      "id": "string",
      "language": "string",
      "last_modified_time": "2026-05-07T12:00:00.000Z",
      "session_type": "string",
      "speaker_to_be_announced": true,
      "start_time": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "track": "string",
      "venue": "string",
      "venue_to_be_announced": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda` | string |  |
| `created_time` | date |  |
| `description` | string |  |
| `duration` | number |  |
| `featured` | boolean |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `language` | string |  |
| `last_modified_time` | date |  |
| `session_type` | string |  |
| `speaker_to_be_announced` | boolean |  |
| `start_time` | date |  |
| `title` | string |  |
| `track` | string |  |
| `venue` | string |  |
| `venue_to_be_announced` | boolean |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `POST /v3/portals/:portal_id/events/:event_id/sessions` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

