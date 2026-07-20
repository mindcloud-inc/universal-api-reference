# retailCRM: Create Task

Creates a new task in retailCRM.

```
POST https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site": "string",
  "task.text": "string",
  "task.datetime": "string",
  "task.performerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site": "string",
    "task.text": "string",
    "task.datetime": "string",
    "task.performerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site` | list | yes |  |
| `task.text` | string | yes |  |
| `task.commentary` | string | no |  |
| `task.datetime` | string | yes |  |
| `task.performerId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native retailCRM API, this operation is `POST /tasks/create` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

