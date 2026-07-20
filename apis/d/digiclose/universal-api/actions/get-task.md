# Digiclose: Get Task



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-task?${params}`, {
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
| `taskId` | number | yes | Unique identifier for the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "categoryName": "Ava Chen",
      "completedAt": {},
      "contactId": 1,
      "creatorId": 1,
      "description": "string",
      "dueAt": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number |  |
| `categoryName` | string |  |
| `completedAt` | object |  |
| `contactId` | number |  |
| `creatorId` | number |  |
| `description` | string |  |
| `dueAt` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Digiclose API, this operation is `GET /tasks/:task_id` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

