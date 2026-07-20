# GoodDay.work: Get Task

Retrieves a single task from GoodDay.work.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=m0zdHP" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "m0zdHP"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | GoodDay task ID. Default: `m0zdHP`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionRequiredUserId": "string",
      "assignedToUserId": "string",
      "createdByUserId": "string",
      "estimate": 1,
      "id": "string",
      "momentCreated": "string",
      "name": "Ava Chen",
      "priority": 1,
      "progress": 1,
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionRequiredUserId` | string | User currently required to act. |
| `assignedToUserId` | string | Assigned user ID. |
| `createdByUserId` | string | User who created the task. |
| `estimate` | number | Task estimate in minutes. |
| `id` | string | Task ID. |
| `momentCreated` | string | Creation timestamp. |
| `name` | string | Task title. |
| `priority` | number | Task priority. |
| `progress` | number | Task progress percentage. |
| `projectId` | string | Associated project ID. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /task/:taskId` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

