# Dart: Move Task

Moves a task within a Dart dartboard.

```
PUT https://connect.mindcloud.co/v1/universal/dart/latest/actions/move-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dart/latest/actions/move-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dart/latest/actions/move-task', {
  method: 'PUT',
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
| `afterTaskId` | string | no |  |
| `beforeTaskId` | string | no |  |
| `id` | string | no |  |

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

Through the native Dart API, this operation is `POST /tasks/:id/move` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-task.md) for the provider-specific parameters and requirements.

