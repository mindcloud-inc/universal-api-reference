# Google Tasks: Get Task

Retrieves a task from Google Tasks.

```
GET https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Tasks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/get-task?connectionId=$CONNECTION_ID&tasklist=string&task=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tasklist": "string",
  "task": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/get-task?${params}`, {
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
| `tasklist` | list | yes |  |
| `task` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string",
      "kind": "string",
      "links": [
        {
          "description": "https://example.com",
          "link": "https://example.com",
          "type": "https://example.com"
        }
      ],
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
| `links[].description` | string |  |
| `links[].link` | string |  |
| `links[].type` | string |  |
| `position` | string |  |
| `selfLink` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `webViewLink` | string |  |

## Native endpoint

Through the native Google Tasks API, this operation is `GET /lists/:tasklist/tasks/:task` (base URL `https://tasks.googleapis.com/tasks/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

