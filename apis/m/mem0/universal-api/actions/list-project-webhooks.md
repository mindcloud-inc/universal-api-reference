# Mem0: List Project Webhooks

Retrieves project webhooks from Mem0.

```
GET https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-project-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-project-webhooks?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-project-webhooks?${params}`, {
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
| `project_id` | string | yes | Mem0 project ID from the webhook resource path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "event_types": [
        "string"
      ],
      "is_active": true,
      "name": "Ava Chen",
      "project": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webhook_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `event_types` | array<string> |  |
| `is_active` | boolean |  |
| `name` | string |  |
| `project` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `webhook_id` | string |  |

## Native endpoint

Through the native Mem0 API, this operation is `GET /api/v1/webhooks/projects/:project_id/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-webhooks.md) for the provider-specific parameters and requirements.

