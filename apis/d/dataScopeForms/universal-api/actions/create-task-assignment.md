# DataScope Forms: Create Task Assignment

Creates a task assignment in DataScope Forms.

```
POST https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-task-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-task-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "string",
  "form_id": 1,
  "user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-task-assignment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "string",
    "form_id": 1,
    "user_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `c_code` | string | no | Company tax ID or code of the location. |
| `c_name` | string | no | Company name of the location. |
| `code` | string | no | Code to identify the task. |
| `date` | string | yes | Date and time of the assigned task in YYYY-mm-dd HH:MM format. |
| `form_id` | number | yes | Internal identifier of the form to assign. |
| `gap` | number | no | Hours available to perform the task. |
| `l_code` | string | no | Code of the location for the task. |
| `l_email` | string | no | Email address of the location. |
| `l_phone` | string | no | Phone number of the location. |
| `latitude` | number | no | Latitude of the location. |
| `location_address` | string | no | Address of the location. |
| `location_name` | string | no | Name of the location when it needs to be created or updated. |
| `longitude` | number | no | Longitude of the location. |
| `task_instruction` | string | no | Instruction shown on the assigned task. |
| `user_id` | string | yes | Email address of the user assigned to the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "task": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `task` | object |  |

## Native endpoint

Through the native DataScope Forms API, this operation is `POST /external/assign_task` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-assignment.md) for the provider-specific parameters and requirements.

