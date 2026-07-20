# TeamBook: Create Actual Logs

Creates new actual logs in TeamBook.

```
POST https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-actual-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-actual-logs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-actual-logs', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "id": "string",
      "payroll_item": {
        "id": 1,
        "name": "Ava Chen"
      },
      "project": {
        "code": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "task": {
        "id": 1,
        "name": "Ava Chen"
      },
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user": {
        "email": "ava@example.com",
        "id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `created_at` | date |  |
| `date` | date |  |
| `duration` | string |  |
| `id` | string |  |
| `payroll_item.id` | number |  |
| `payroll_item.name` | string |  |
| `project.code` | string |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `task.id` | number |  |
| `task.name` | string |  |
| `updated_at` | date |  |
| `user.email` | string |  |
| `user.id` | number |  |

## Native endpoint

Through the native TeamBook API, this operation is `POST /actual_logs` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-actual-logs.md) for the provider-specific parameters and requirements.

