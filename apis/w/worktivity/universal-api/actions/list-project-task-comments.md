# Worktivity: List Project Task Comments

Retrieves project task comments from Worktivity.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-project-task-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-project-task-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-project-task-comments?${params}`, {
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
      "comment": "string",
      "createdBy": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isChangelog": true,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdBy` | string |  |
| `createdDate` | date |  |
| `id` | string |  |
| `isChangelog` | boolean |  |
| `taskId` | string |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Project/ListComments` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-task-comments.md) for the provider-specific parameters and requirements.

