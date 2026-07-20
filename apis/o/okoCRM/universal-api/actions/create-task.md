# OkoCRM: Create task

Creates a new task in OkoCRM.

```
POST https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "executor_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "executor_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company_id` | number | no | Company ID to attach the task to. |
| `contact_id` | number | no | Contact ID to attach the task to. |
| `executor_id` | number | yes | The user assigned to the task. |
| `lead_id` | number | no | Deal ID to attach the task to. Provide one of deal, contact, or company. |
| `text` | string | no | Task text. Provide this or a task type ID. |
| `type_id` | number | no | Task type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `POST /tasks/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

