# Grain: List Recordings

Retrieves recordings from Grain.

```
GET https://connect.mindcloud.co/v1/universal/grain/latest/actions/list-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grain `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grain/latest/actions/list-recordings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grain/latest/actions/list-recordings?${params}`, {
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
| `filter.after_datetime` | date | no | Only return recordings whose start_datetime is before this timestamp, per Grain's Recording Filter docs. |
| `filter.before_datetime` | date | no | Only return recordings whose start_datetime is after this timestamp, per Grain's Recording Filter docs. |
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
| `include` | object | no | Optional related entities to include in response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "durationMs": 1,
      "endDatetime": "string",
      "id": "string",
      "mediaType": "string",
      "meetingType": {
        "id": "string",
        "name": "Ava Chen",
        "scope": "string"
      },
      "source": "string",
      "startDatetime": "string",
      "teams": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
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
| `durationMs` | number |  |
| `endDatetime` | string |  |
| `id` | string |  |
| `mediaType` | string |  |
| `meetingType.id` | string |  |
| `meetingType.name` | string |  |
| `meetingType.scope` | string |  |
| `source` | string |  |
| `startDatetime` | string |  |
| `teams[].id` | string |  |
| `teams[].name` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Grain API, this operation is `POST /v2/recordings` (base URL `https://api.grain.com/_/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recordings.md) for the provider-specific parameters and requirements.

