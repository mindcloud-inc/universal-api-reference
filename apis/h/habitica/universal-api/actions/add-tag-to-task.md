# Habitica: Add Tag To Task

Adds a tag to a Habitica task.

```
PUT https://connect.mindcloud.co/v1/universal/habitica/latest/actions/add-tag-to-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/add-tag-to-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "tagId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/habitica/latest/actions/add-tag-to-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "tagId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The Habitica task ID. |
| `tagId` | string | yes | The Habitica tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklist": [
        {}
      ],
      "completed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "notes": "string",
      "priority": 1,
      "tags": [
        "string"
      ],
      "text": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checklist` | array<object> |  |
| `completed` | boolean |  |
| `createdAt` | date |  |
| `id` | string |  |
| `notes` | string |  |
| `priority` | number |  |
| `tags` | array<string> |  |
| `text` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Habitica API, this operation is `POST /tasks/:taskId/tags/:tagId` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tag-to-task.md) for the provider-specific parameters and requirements.

