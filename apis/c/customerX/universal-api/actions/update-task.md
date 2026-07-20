# CustomerX: Update Task

Updates an existing task in CustomerX.

```
PUT https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-task', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "client_id": 1,
      "created_at": "string",
      "dashboard_activities_step_id": 1,
      "date": "string",
      "date_scheduled": "string",
      "date_scheduled_final": "string",
      "description": "string",
      "id": 1,
      "position": 1,
      "status": true,
      "title": "string",
      "updated_at": "string",
      "user": {},
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `dashboard_activities_step_id` | number |  |
| `date` | string |  |
| `date_scheduled` | string |  |
| `date_scheduled_final` | string |  |
| `description` | string |  |
| `id` | number |  |
| `position` | number |  |
| `status` | boolean |  |
| `title` | string |  |
| `updated_at` | string |  |
| `user` | object |  |
| `user_id` | number |  |

## Native endpoint

Through the native CustomerX API, this operation is `PUT /api/v1/tasks/[:id]` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

