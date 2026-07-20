# ProProfs Project: List Files

Retrieves a list of files from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-files?${params}`, {
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
| `limit` | string | no | Limit the number of returned files. |
| `offset` | string | no | Offset for returned files. |
| `order` | string | no | Sort order for returned files. |
| `projectId` | string | no | Filter files by project. |
| `subtaskId` | string | no | Filter files by subtask. |
| `taskId` | string | no | Filter files by task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "commentId": "string",
          "dateCreated": "string",
          "dateModified": "string",
          "fileName": "Ava Chen",
          "filePath": "string",
          "hash": "string",
          "projectId": "string",
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
| `data[].commentId` | string |  |
| `data[].dateCreated` | string |  |
| `data[].dateModified` | string |  |
| `data[].fileName` | string |  |
| `data[].filePath` | string |  |
| `data[].hash` | string |  |
| `data[].projectId` | string |  |
| `data[].subtaskId` | string |  |
| `data[].taskId` | string |  |
| `data[].userId` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /files` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

