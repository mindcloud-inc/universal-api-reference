# Microsoft 365 Planner: Get Task



```
GET https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=01gzSlKkIUSUl6DF_EilrmQAKDhh" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "01gzSlKkIUSUl6DF_EilrmQAKDhh"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | Planner task ID to retrieve. Example: `01gzSlKkIUSUl6DF_EilrmQAKDhh`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketId": "string",
      "dueDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "percentComplete": 1,
      "planId": "string",
      "priority": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `dueDateTime` | date |  |
| `id` | string |  |
| `percentComplete` | number |  |
| `planId` | string |  |
| `priority` | number |  |
| `startDateTime` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `GET /v1.0/planner/tasks/{{taskId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

