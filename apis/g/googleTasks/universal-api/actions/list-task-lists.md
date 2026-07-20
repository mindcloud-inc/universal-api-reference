# Google Tasks: List Task Lists

Finds task lists in Google Tasks.

```
GET https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-task-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Tasks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-task-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-task-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string",
      "kind": "string",
      "selfLink": "https://example.com",
      "title": "string",
      "updated": "string"
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
| `selfLink` | string |  |
| `title` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Google Tasks API, this operation is `GET /users/@me/lists` (base URL `https://tasks.googleapis.com/tasks/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-task-lists.md) for the provider-specific parameters and requirements.

