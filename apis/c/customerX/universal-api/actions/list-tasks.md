# CustomerX: List Tasks

Retrieves a list of tasks from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "additional_contacts": [
        "string"
      ],
      "client": {},
      "client_id": 1,
      "created_at": "string",
      "dashboard_activities_step_id": 1,
      "date": "string",
      "date_scheduled": "string",
      "date_scheduled_final": "string",
      "description": "string",
      "id": 1,
      "labels": [
        {}
      ],
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
| `additional_contacts` | array<string> |  |
| `client` | object |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `dashboard_activities_step_id` | number |  |
| `date` | string |  |
| `date_scheduled` | string |  |
| `date_scheduled_final` | string |  |
| `description` | string |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `position` | number |  |
| `status` | boolean |  |
| `title` | string |  |
| `updated_at` | string |  |
| `user` | object |  |
| `user_id` | number |  |

## Native endpoint

Through the native CustomerX API, this operation is `GET /api/v1/tasks` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

