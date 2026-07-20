# Umbrella: Count Active Alerts

Retrieves the count of active alerts from Umbrella.

```
GET https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/count-active-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/count-active-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/count-active-alerts?${params}`, {
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
      "severityCounts": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `severityCounts` | object |  |
| `total` | number |  |

## Native endpoint

Through the native Umbrella API, this operation is `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"only_active_alerts_count":true}` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-active-alerts.md) for the provider-specific parameters and requirements.

