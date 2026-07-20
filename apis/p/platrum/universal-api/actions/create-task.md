# Platrum: Create task

Creates a new task in Platrum.

```
POST https://connect.mindcloud.co/v1/universal/platrum/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platrum/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `board_panel_id` | number | no | Board panel ID. |
| `description` | string | no | Task description. |
| `finish_date` | date | no | Task finish date. |
| `name` | string | no | Task name. |
| `owner_user_id` | string | no | Task owner user ID. |
| `responsible_user_ids[]` | array<string> | no | Responsible user IDs. |
| `start_date` | date | no | Task start date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /tasks/api/task/create` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

