# Kiwili: Create Task

Creates a new task in Kiwili.

```
POST https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "EnterpriseId": 1,
  "ProjectId": 1,
  "Summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "EnterpriseId": 1,
    "ProjectId": 1,
    "Summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Active` | boolean | no | Whether the task is active. |
| `EnterpriseId` | number | yes | The enterprise ID for the task. |
| `ProjectId` | number | yes | The project ID for the task. |
| `Summary` | string | yes | The task summary. |

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

Through the native Kiwili API, this operation is `POST /task` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

