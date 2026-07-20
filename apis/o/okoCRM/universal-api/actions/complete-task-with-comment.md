# OkoCRM: Complete task with comment

Marks a task as done in OkoCRM with a comment.

```
PUT https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/complete-task-with-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/complete-task-with-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/complete-task-with-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The OkoCRM task ID. |
| `text` | string | no | Comment to leave when completing the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `POST /tasks/done/[:id]` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-task-with-comment.md) for the provider-specific parameters and requirements.

