# DoneDone: Update Task Priority

Updates an existing task priority in DoneDone.

```
PUT https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/update-task-priority
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/update-task-priority" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "taskId": 1,
  "priorityId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/update-task-priority', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "taskId": 1,
    "priorityId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | DoneDone account ID. |
| `projectId` | number | yes | DoneDone internal project ID. |
| `taskId` | number | yes | DoneDone task ID. |
| `priorityId` | number | yes | Task priority ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider confirmation message. |

## Native endpoint

Through the native DoneDone API, this operation is `PUT /:account_id/internal-projects/:internal_project_id/tasks/:task_id/priority` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-priority.md) for the provider-specific parameters and requirements.

