# Grain: Create Hook

Creates a new hook in Grain.

```
POST https://connect.mindcloud.co/v1/universal/grain/latest/actions/create-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grain/latest/actions/create-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hook_url": "https://example.com",
  "hook_type": "highlight_added"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grain/latest/actions/create-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hook_url": "https://example.com",
    "hook_type": "highlight_added"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hook_url` | string | yes |  |
| `include.ai_action_items` | boolean | no | Include AI action items in hook payloads. |
| `include.ai_summary` | boolean | no | Include AI summary in hook payloads. |
| `include.ai_template_sections` | object | no | Include AI template sections in hook payloads. |
| `include.ai_template_sections.allowed_sections[]` | array<string> | no | Only include AI template sections whose title matches one of these values. |
| `include.ai_template_sections.format` | list | no | Output format for AI template sections in hook payloads. One of: `json`, `markdown`, `text`. |
| `include.calendar_event` | boolean | no | Include calendar event data in hook payloads. |
| `include.highlights` | boolean | no | Include clips/highlights in hook payloads. |
| `include.hubspot` | boolean | no | Include HubSpot related data in hook payloads. |
| `include.participants` | boolean | no | Include participants in hook payloads. |
| `include.private_notes` | boolean | no | Include private notes in hook payloads. |
| `include.speakers` | boolean | no | Include highlight speakers in hook payloads. |
| `include.transcript` | boolean | no | Include highlight transcript in hook payloads. |
| `hook_type` | list | yes | One of: `highlight_added`, `highlight_deleted`, `highlight_updated`, `recording_added`, `recording_deleted`, `recording_updated`, `story_added`, `story_deleted`, `story_updated`, `upload_status`. |
| `include` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "hookType": "string",
      "hookUrl": "https://example.com",
      "id": "string",
      "include": {},
      "insertedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `hookType` | string |  |
| `hookUrl` | string |  |
| `id` | string |  |
| `include` | object |  |
| `insertedAt` | date |  |

## Native endpoint

Through the native Grain API, this operation is `POST /v2/hooks/create` (base URL `https://api.grain.com/_/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-hook.md) for the provider-specific parameters and requirements.

