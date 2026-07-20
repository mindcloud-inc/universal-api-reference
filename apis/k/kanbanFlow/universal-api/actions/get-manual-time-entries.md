# KanbanFlow: Get manual time entries

Retrieves all manual time entries for a KanbanFlow task.

```
GET https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-manual-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-manual-time-entries?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-manual-time-entries?${params}`, {
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
| `taskId` | string | yes | The KanbanFlow task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdTimestamp": "string",
      "endTimestamp": "string",
      "startTimestamp": "string",
      "taskId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdTimestamp` | string |  |
| `endTimestamp` | string |  |
| `startTimestamp` | string |  |
| `taskId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native KanbanFlow API, this operation is `GET /tasks/:taskId/manual-time-entries` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-manual-time-entries.md) for the provider-specific parameters and requirements.

