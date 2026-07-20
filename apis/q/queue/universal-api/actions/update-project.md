# Queue: Update Project

Updates an existing project in Queue.

```
PUT https://connect.mindcloud.co/v1/universal/queue/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/queue/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/queue/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archive": "string",
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "private": true,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archive` | string |  |
| `avatar` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `private` | boolean |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Queue API, this operation is `PATCH projects/:project_id` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

