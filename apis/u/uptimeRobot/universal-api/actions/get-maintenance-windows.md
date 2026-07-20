# UptimeRobot: Get Maintenance Windows

Retrieves maintenance windows and details from UptimeRobot.

```
GET https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-maintenance-windows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UptimeRobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-maintenance-windows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/get-maintenance-windows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mwindows` | string | no | Optional dash-separated maintenance window IDs to filter. |
| `offset` | number | no | Pagination offset. |
| `limit` | number | no | Pagination limit, max 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mwindows": [
        {}
      ],
      "pagination": {},
      "stat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mwindows` | array<object> |  |
| `pagination` | object |  |
| `stat` | string |  |

## Native endpoint

Through the native UptimeRobot API, this operation is `POST /getMWindows` (base URL `https://api.uptimerobot.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-maintenance-windows.md) for the provider-specific parameters and requirements.

