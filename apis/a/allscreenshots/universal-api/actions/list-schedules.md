# Allscreenshots: List Schedules

Retrieves recurring screenshot schedules from Allscreenshots.

```
GET https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/list-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/list-schedules?${params}`, {
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
      "lastRunAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextRunAt": "2026-05-07T12:00:00.000Z",
      "schedule": "string",
      "scheduleId": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastRunAt` | date |  |
| `name` | string |  |
| `nextRunAt` | date |  |
| `schedule` | string |  |
| `scheduleId` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `GET /v1/schedules` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedules.md) for the provider-specific parameters and requirements.

