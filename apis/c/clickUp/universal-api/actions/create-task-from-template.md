# ClickUp: Create Task From Template

Creates a task from a ClickUp task template.

```
POST https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "templateId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-task-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "templateId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes |  |
| `templateId` | string | yes |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": {
        "status": "string",
        "type": "string"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `dateUpdated` | date |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status.status` | string |  |
| `status.type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `POST list/:list_id/taskTemplate/:template_id` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-from-template.md) for the provider-specific parameters and requirements.

