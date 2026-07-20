# Vybit: Get Usage Metrics



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-usage-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-usage-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-usage-metrics?${params}`, {
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
      "cap_daily": 1,
      "cap_monthly": 1,
      "cap_vybits": 1,
      "count_daily": 1,
      "count_monthly": 1,
      "monthly_reset_dts": "2026-05-07T12:00:00.000Z",
      "number_vybits": 1,
      "tier_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cap_daily` | number | Daily notification capacity for the current tier. |
| `cap_monthly` | number | Monthly notification capacity for the current tier. |
| `cap_vybits` | number | Maximum number of vybits allowed on the current tier. |
| `count_daily` | number | Notifications sent today. |
| `count_monthly` | number | Notifications sent this month. |
| `monthly_reset_dts` | date | When the monthly notification counter resets. |
| `number_vybits` | number | Current count of owned vybits. |
| `tier_id` | number | Current Vybit subscription tier id. |

## Native endpoint

Through the native Vybit API, this operation is `GET /meter` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-metrics.md) for the provider-specific parameters and requirements.

