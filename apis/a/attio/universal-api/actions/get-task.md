# Attio: Get Task

Retrieves a task from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-task?connectionId=$CONNECTION_ID&task_id=649e34f4-c39a-4f4d-99ef-48a36bef8f04" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "649e34f4-c39a-4f4d-99ef-48a36bef8f04"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-task?${params}`, {
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
| `task_id` | string | yes | The ID of the task to retrieve. Example: `649e34f4-c39a-4f4d-99ef-48a36bef8f04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "contentPlaintext": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByActor": {},
      "deadlineAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "isCompleted": true,
      "linkedRecords": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> | Task assignees. |
| `contentPlaintext` | string | Plaintext task content. |
| `createdAt` | date | When the task was created. |
| `createdByActor` | object | Actor that created the task. |
| `deadlineAt` | date | Task deadline timestamp, when set. |
| `id` | object | Task identifier payload containing workspace and task ids. |
| `isCompleted` | boolean | Whether the task is completed. |
| `linkedRecords` | array<object> | Records linked to the task. |

## Native endpoint

Through the native Attio API, this operation is `GET /v2/tasks/:task_id` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

