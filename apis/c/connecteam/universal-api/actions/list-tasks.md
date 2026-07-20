# Connecteam: List Tasks

Retrieves a list of tasks under a specified task board

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&taskBoardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "taskBoardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-tasks?${params}`, {
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
| `taskBoardId` | string | yes |  |
| `taskIds` | array<string> | no | Accepts multiple values as an array. |
| `labelIds` | array<string> | no | Accepts multiple values as an array. |
| `userIds` | array<number> | no | Accepts multiple values as an array. |
| `status` | string | no |  |
| `limit` | number | no | Default: `10`. |
| `offset` | number | no | Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dueDate": 1,
      "id": "string",
      "isArchived": true,
      "labelIds": [
        "string"
      ],
      "startTime": 1,
      "status": "string",
      "title": "string",
      "type": "string",
      "userIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dueDate` | number |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `labelIds[]` | string |  |
| `startTime` | number |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userIds[]` | number |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /tasks/v1/taskboards/:taskBoardId/tasks` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

