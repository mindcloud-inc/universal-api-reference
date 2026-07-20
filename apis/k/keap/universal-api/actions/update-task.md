# Keap: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigned_to_user_id` | string | no |  |
| `completed` | string | no |  |
| `completion_time` | string | no |  |
| `contact_id` | string | no |  |
| `description` | string | no |  |
| `due_time` | string | no |  |
| `priority` | string | no |  |
| `remind_time_mins` | string | no |  |
| `task_id` | string | yes | The unique identifier of the task. |
| `title` | string | no |  |
| `type` | string | no |  |
| `update_mask` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "completed": "string",
      "completionTime": "string",
      "contactId": "string",
      "createdByUserId": "string",
      "createTime": "string",
      "description": "string",
      "dueTime": "string",
      "id": "string",
      "modificationTime": "string",
      "priority": "string",
      "remindTimeMins": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | string |  |
| `completed` | string |  |
| `completionTime` | string |  |
| `contactId` | string |  |
| `createdByUserId` | string |  |
| `createTime` | string |  |
| `description` | string |  |
| `dueTime` | string |  |
| `id` | string |  |
| `modificationTime` | string |  |
| `priority` | string |  |
| `remindTimeMins` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Keap API, this operation is `PATCH /tasks/{task_id}` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

