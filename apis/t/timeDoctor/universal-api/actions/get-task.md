# Time Doctor: Get Task

Retrieves a task from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | ID of the task to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "integration": {},
      "name": "Ava Chen",
      "project": {},
      "reporterId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `integration` | object |  |
| `name` | string |  |
| `project` | object |  |
| `reporterId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/tasks/:taskId` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

