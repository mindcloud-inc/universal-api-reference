# BASIC: Get project activity stats

Retrieves project activity stats from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-activity-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-activity-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-activity-stats?${params}`, {
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
      "dau": 1,
      "mau": 1,
      "series": [
        {
          "active_users": 1,
          "date": "2026-05-07T12:00:00.000Z"
        }
      ],
      "total": 1,
      "wau": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dau` | number |  |
| `mau` | number |  |
| `series[].active_users` | number |  |
| `series[].date` | date |  |
| `total` | number |  |
| `wau` | number |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /project/{id}/user/stats` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-activity-stats.md) for the provider-specific parameters and requirements.

