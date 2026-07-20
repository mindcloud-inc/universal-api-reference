# Google Tasks: Create Task

Creates a new task in Google Tasks.

```
POST https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Tasks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasklist": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasklist": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tasklist` | list | yes |  |
| `title` | string | no |  |
| `notes` | string | no |  |
| `due` | date | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent` | string | no |  |
| `previous` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string",
      "kind": "string",
      "notes": "string",
      "position": "string",
      "selfLink": "https://example.com",
      "status": "string",
      "title": "string",
      "updated": "string",
      "webViewLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `notes` | string |  |
| `position` | string |  |
| `selfLink` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `webViewLink` | string |  |

## Native endpoint

Through the native Google Tasks API, this operation is `POST /lists/:tasklist/tasks` (base URL `https://tasks.googleapis.com/tasks/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

