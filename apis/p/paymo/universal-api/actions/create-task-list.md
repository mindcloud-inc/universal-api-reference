# Paymo: Create Task List

Creates a task list in Paymo.

```
POST https://connect.mindcloud.co/v1/universal/paymo/latest/actions/create-task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/create-task-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "project_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paymo/latest/actions/create-task-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "project_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The task list name. |
| `project_id` | number | yes | The Paymo project id the task list belongs to. |

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

Through the native Paymo API, this operation is `POST tasklists` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-list.md) for the provider-specific parameters and requirements.

