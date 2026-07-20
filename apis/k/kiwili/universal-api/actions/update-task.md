# Kiwili: Update Task

Updates an existing task in Kiwili.

```
PUT https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Active` | boolean | no | Whether the task is active. |
| `EnterpriseId` | number | no | The enterprise ID for the task. |
| `ProjectId` | number | no | The project ID for the task. |
| `Summary` | string | no | The updated task summary. |
| `task_id` | number | yes | The Kiwili task ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Archive": true,
      "EnterpriseId": 1,
      "Id": 1,
      "ProjectId": 1,
      "Status": "string",
      "Summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Archive` | boolean |  |
| `EnterpriseId` | number |  |
| `Id` | number |  |
| `ProjectId` | number |  |
| `Status` | string |  |
| `Summary` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `PUT /task/:task_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

