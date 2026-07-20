# Grain: Get Recording

Retrieves a recording from Grain.

```
GET https://connect.mindcloud.co/v1/universal/grain/latest/actions/get-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grain/latest/actions/get-recording?connectionId=$CONNECTION_ID&recording_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recording_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grain/latest/actions/get-recording?${params}`, {
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
| `include.ai_action_items` | boolean | no | Include AI action items in the response. |
| `include.ai_summary` | boolean | no | Include AI summary in the response. |
| `include.ai_template_sections` | object | no | Include AI template sections in the response. |
| `include.ai_template_sections.allowed_sections[]` | array<string> | no | Only include AI template sections whose title matches one of these values. |
| `include.ai_template_sections.format` | list | no | Output format for AI template sections. One of: `json`, `markdown`, `text`. |
| `include.calendar_event` | boolean | no | Include calendar event data in the response. |
| `include.highlights` | boolean | no | Include clips/highlights in the response. |
| `include.hubspot` | boolean | no | Include HubSpot related data in the response. |
| `include.participants` | boolean | no | Include participants in the response. |
| `include.private_notes` | boolean | no | Include private notes in the response. |
| `recording_id` | list<string> | yes |  |
| `include` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiActionItems": [
        {}
      ],
      "aiSummary": {},
      "aiTemplateSections": [
        {}
      ],
      "calendarEvent": {},
      "durationMs": 1,
      "endDatetime": "2026-05-07T12:00:00.000Z",
      "highlights": [
        {}
      ],
      "hubspot": {},
      "id": "string",
      "mediaType": "string",
      "meetingType": {},
      "participants": [
        {}
      ],
      "privateNotes": {},
      "source": "string",
      "startDatetime": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "teams": [
        {}
      ],
      "thumbnailUrl": "https://example.com",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiActionItems` | array<object> |  |
| `aiSummary` | object |  |
| `aiTemplateSections` | array<object> |  |
| `calendarEvent` | object |  |
| `durationMs` | number |  |
| `endDatetime` | date |  |
| `highlights` | array<object> |  |
| `hubspot` | object |  |
| `id` | string |  |
| `mediaType` | string |  |
| `meetingType` | object |  |
| `participants` | array<object> |  |
| `privateNotes` | object |  |
| `source` | string |  |
| `startDatetime` | date |  |
| `tags` | array<string> |  |
| `teams` | array<object> |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Grain API, this operation is `POST /v2/recordings/:recording_id` (base URL `https://api.grain.com/_/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recording.md) for the provider-specific parameters and requirements.

