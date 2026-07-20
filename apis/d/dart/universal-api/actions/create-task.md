# Dart: Create Task

Creates a new task in Dart.

```
POST https://connect.mindcloud.co/v1/universal/dart/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dart/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dart/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item.assignee` | string | no |  |
| `item.dartboard` | string | no |  |
| `item.description` | string | no |  |
| `item.dueAt` | string | no |  |
| `item.priority` | string | no |  |
| `item.startAt` | string | no |  |
| `item.status` | string | no |  |
| `item.tags` | string | no |  |
| `item.title` | string | no |  |
| `item.type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dartboard": "string",
      "description": "string",
      "htmlUrl": "https://example.com",
      "id": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "title": "string",
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
| `createdAt` | date |  |
| `dartboard` | string |  |
| `description` | string |  |
| `htmlUrl` | string |  |
| `id` | string |  |
| `status` | string |  |
| `tags[]` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Dart API, this operation is `POST /tasks` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

