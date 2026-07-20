# Queue: Get Projects

Retrieves projects from Queue.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-projects?${params}`, {
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

Through the native Queue API, this operation is `GET projects` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-projects.md) for the provider-specific parameters and requirements.

