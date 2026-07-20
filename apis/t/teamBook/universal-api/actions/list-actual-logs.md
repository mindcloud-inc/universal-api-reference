# TeamBook: List Actual Logs

Retrieves actual log records from TeamBook.

```
GET https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-actual-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-actual-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-actual-logs?${params}`, {
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

Through the native TeamBook API, this operation is `GET /actual_logs` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-actual-logs.md) for the provider-specific parameters and requirements.

