# ProProfs Project: List Comments

Retrieves a list of comments from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-comments?${params}`, {
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
| `limit` | string | no | Limit the number of returned comments. |
| `offset` | string | no | Offset for returned comments. |
| `projectId` | string | no | Filter comments by project ID. |
| `subtaskId` | string | no | Filter comments by subtask ID. |
| `taskId` | string | no | Filter comments by task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "comment": "string",
          "commentId": "string",
          "dateCreated": "string",
          "dateModified": "string",
          "filename": "Ava Chen",
          "filepath": "string",
          "note": "string",
          "parentId": "string",
          "projectId": "string",
          "replies": [
            {
              "comment": "string",
              "commentId": "string",
              "dateCreated": "string",
              "dateModified": "string",
              "parentId": "string",
              "projectId": "string",
              "subtaskId": "string",
              "taskId": "string",
              "userId": "string"
            }
          ],
          "subtaskId": "string",
          "taskId": "string",
          "userId": "string"
        }
      ],
      "paging": {
        "limit": 1,
        "offset": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].comment` | string |  |
| `data[].commentId` | string |  |
| `data[].dateCreated` | string |  |
| `data[].dateModified` | string |  |
| `data[].filename` | string |  |
| `data[].filepath` | string |  |
| `data[].note` | string |  |
| `data[].parentId` | string |  |
| `data[].projectId` | string |  |
| `data[].replies[].comment` | string |  |
| `data[].replies[].commentId` | string |  |
| `data[].replies[].dateCreated` | string |  |
| `data[].replies[].dateModified` | string |  |
| `data[].replies[].parentId` | string |  |
| `data[].replies[].projectId` | string |  |
| `data[].replies[].subtaskId` | string |  |
| `data[].replies[].taskId` | string |  |
| `data[].replies[].userId` | string |  |
| `data[].subtaskId` | string |  |
| `data[].taskId` | string |  |
| `data[].userId` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /comments` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

