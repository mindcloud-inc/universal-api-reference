# Recallai: List Calendar Events

Retrieves calendar events from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-calendar-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-calendar-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-calendar-events?${params}`, {
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
| `calendarId` | string | no | Calendar ID |
| `cursor` | string | no | The pagination cursor value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bots": [
        {}
      ],
      "calendar_id": "string",
      "created_at": "string",
      "end_time": "string",
      "ical_uid": "string",
      "id": "string",
      "is_deleted": true,
      "meeting_platform": {},
      "meeting_url": "https://example.com",
      "platform": "string",
      "platform_id": "string",
      "raw": "string",
      "start_time": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bots` | array<object> |  |
| `calendar_id` | string |  |
| `created_at` | string |  |
| `end_time` | string |  |
| `ical_uid` | string |  |
| `id` | string |  |
| `is_deleted` | boolean |  |
| `meeting_platform` | object |  |
| `meeting_url` | string |  |
| `platform` | string |  |
| `platform_id` | string |  |
| `raw` | string |  |
| `start_time` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `GET /api/v2/calendar-events/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-events.md) for the provider-specific parameters and requirements.

