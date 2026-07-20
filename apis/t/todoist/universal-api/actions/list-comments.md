# Todoist: List Comments

Retrieves comments from Todoist.

```
GET https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-comments?${params}`, {
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
| `projectId` | string | no | Project ID to list comments from. Use either Project ID or Task ID. |
| `taskId` | string | no | Task ID to list comments from. Use either Task ID or Project ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Cursor for the next page of results. |
| `limit` | number | no | Maximum number of results to return. |
| `publicKey` | string | no | Public key used for shared-resource access where applicable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "fileAttachment": {},
      "id": "string",
      "postedAt": "2026-05-07T12:00:00.000Z",
      "postedUid": "string",
      "projectId": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Comment content |
| `fileAttachment` | object | Attached file metadata when present |
| `id` | string | Comment ID |
| `postedAt` | date | Comment creation timestamp |
| `postedUid` | string | User ID that posted the comment |
| `projectId` | string | Project ID for the comment |
| `taskId` | string | Task ID for the comment |

## Native endpoint

Through the native Todoist API, this operation is `GET /api/v1/comments` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

