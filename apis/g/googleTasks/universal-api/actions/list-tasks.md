# Google Tasks: List Tasks

Finds tasks in a Google Tasks list.

```
GET https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Tasks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&tasklist=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tasklist": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-tasks?${params}`, {
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
| `showCompleted` | boolean | no |  |
| `showDeleted` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `completedMin` | date | no |  |
| `completedMax` | date | no |  |
| `dueMin` | date | no |  |
| `dueMax` | date | no |  |
| `updatedMin` | date | no |  |
| `showHidden` | boolean | no |  |

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

Through the native Google Tasks API, this operation is `GET /lists/:tasklist/tasks` (base URL `https://tasks.googleapis.com/tasks/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

