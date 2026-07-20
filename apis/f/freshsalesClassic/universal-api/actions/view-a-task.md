# Freshsales Classic: View a Task

Retrieves a task from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-task?${params}`, {
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
| `id` | number | yes | The task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDate": "string",
      "createdAt": "string",
      "createrId": 1,
      "description": "string",
      "dueDate": "string",
      "hasMultipleEmails": true,
      "id": 1,
      "isLinkedinType": true,
      "outcomeId": 1,
      "ownerId": 1,
      "status": 1,
      "targetables": [
        {}
      ],
      "targetablesWithEmail": [
        {}
      ],
      "taskTypeId": 1,
      "title": "string",
      "updatedAt": "string",
      "updaterId": 1,
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
| `completedDate` | string |  |
| `createdAt` | string |  |
| `createrId` | number |  |
| `description` | string |  |
| `dueDate` | string |  |
| `hasMultipleEmails` | boolean |  |
| `id` | number |  |
| `isLinkedinType` | boolean |  |
| `outcomeId` | number |  |
| `ownerId` | number |  |
| `status` | number |  |
| `targetables` | array<object> |  |
| `targetablesWithEmail` | array<object> |  |
| `taskTypeId` | number |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updaterId` | number |  |
| `userIds` | array<number> |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /tasks/:id` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-a-task.md) for the provider-specific parameters and requirements.

