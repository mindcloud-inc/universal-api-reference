# Less Annoying CRM: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The task Id to update. |
| `name` | string | no | Updated task name. |
| `dueDate` | date | no | Updated due date. |
| `assignedTo` | string | no | Updated assignee user Id. |
| `calendarId` | string | no | Updated calendar Id. |
| `description` | string | no | Updated task details. |
| `contactId` | string | no | Updated attached contact or company Id, or null to detach. |
| `isComplete` | boolean | no | Mark the task complete or incomplete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Less Annoying CRM API returns.

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

