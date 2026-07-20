# zipBoard: Get Tasks

Retrieves tasks from zipBoard.

```
GET https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-tasks?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-tasks?${params}`, {
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
| `fileId` | string | no | Optional file ID whose tasks should be fetched. |
| `priority` | string | no | Optional task priority filter. |
| `projectId` | string | no | Optional project ID whose tasks should be fetched. |
| `projectId` | string | yes |  |
| `status` | string | no | Optional task status filter. |
| `type` | string | no | Optional task type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": "string",
      "commentText": "string",
      "commentType": "string",
      "project_id": "string",
      "taskId": "string",
      "taskPriority": "string",
      "taskStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | string | Comment identifier. |
| `commentText` | string | Task text. |
| `commentType` | string | Comment type. |
| `project_id` | string | Project identifier. |
| `taskId` | string | Task identifier. |
| `taskPriority` | string | Task priority. |
| `taskStatus` | string | Task status. |

## Native endpoint

Through the native zipBoard API, this operation is `GET /issues/tasks` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tasks.md) for the provider-specific parameters and requirements.

