# Paymo: Get Task List

Retrieves a task list from Paymo.

```
GET https://connect.mindcloud.co/v1/universal/paymo/latest/actions/get-task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/get-task-list?connectionId=$CONNECTION_ID&tasklistId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tasklistId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paymo/latest/actions/get-task-list?${params}`, {
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
| `tasklistId` | number | yes | The Paymo task list id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "milestoneId": 1,
      "name": "Ava Chen",
      "projectId": 1,
      "seq": 1,
      "tasksCount": {},
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `id` | number |  |
| `milestoneId` | number |  |
| `name` | string |  |
| `projectId` | number |  |
| `seq` | number |  |
| `tasksCount` | object |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Paymo API, this operation is `GET tasklists/:tasklistId` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-list.md) for the provider-specific parameters and requirements.

