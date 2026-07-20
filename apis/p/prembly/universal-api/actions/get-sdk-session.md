# Prembly: Get SDK Session

Retrieves SDK sessions from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-sdk-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-sdk-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-sdk-session?${params}`, {
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
      "pagination": {
        "page": 1,
        "page_size": 1,
        "total": 1,
        "total_pages": 1
      },
      "sessions": [
        {
          "completed_at": "2026-05-07T12:00:00.000Z",
          "created_at": "2026-05-07T12:00:00.000Z",
          "currency": "string",
          "duration": 1,
          "end_user_email": "ava@example.com",
          "end_user_phone": "string",
          "failure_reason": "string",
          "full_name": "Ava Chen",
          "id": "string",
          "is_used": true,
          "overall_result": "string",
          "session_id": "string",
          "started_at": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "total_cost": "string",
          "widget_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.page` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total` | number |  |
| `pagination.total_pages` | number |  |
| `sessions[].completed_at` | date |  |
| `sessions[].created_at` | date |  |
| `sessions[].currency` | string |  |
| `sessions[].duration` | number |  |
| `sessions[].end_user_email` | string |  |
| `sessions[].end_user_phone` | string |  |
| `sessions[].failure_reason` | string |  |
| `sessions[].full_name` | string |  |
| `sessions[].id` | string |  |
| `sessions[].is_used` | boolean |  |
| `sessions[].overall_result` | string |  |
| `sessions[].session_id` | string |  |
| `sessions[].started_at` | date |  |
| `sessions[].status` | string |  |
| `sessions[].total_cost` | string |  |
| `sessions[].widget_name` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /api/v1/checker-widget/sdk/sessions/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sdk-session.md) for the provider-specific parameters and requirements.

