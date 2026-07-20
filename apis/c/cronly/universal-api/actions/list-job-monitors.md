# Cronly: List Job Monitors



```
GET https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-job-monitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-job-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-job-monitors?${params}`, {
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
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "id": 1,
      "is_alerted": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "schedule": "string",
      "timezone": "string",
      "token": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `created_at` | date |  |
| `duration` | number |  |
| `id` | number |  |
| `is_alerted` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `schedule` | string |  |
| `timezone` | string |  |
| `token` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Cronly API, this operation is `GET /api/monitors` (base URL `https://cronly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-monitors.md) for the provider-specific parameters and requirements.

