# MILKEE: Create Task

Creates a new task in MILKEE.

```
POST https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "4640",
  "due": "string",
  "projectId": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "4640",
    "due": "string",
    "projectId": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |
| `description` | string | no | Task description. |
| `due` | string | yes | Task due date. |
| `plannedHours` | number | no | Estimated hours to complete the task. |
| `projectId` | number | yes | ID of the project this task belongs to. |
| `status` | string | no | Task status: open, in-progress, or done. |
| `title` | string | yes | Task title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `POST /companies/:companyId/tasks` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

