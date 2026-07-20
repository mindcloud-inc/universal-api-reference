# PagePixels: Get Account Limits



```
GET https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-account-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-account-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/get-account-limits?${params}`, {
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
      "aiAnalysisRequestsCurrentMonthUsage": 1,
      "aiAnalysisRequestsLimit": 1,
      "realLocationBandwidthCurrentMonthUsageInBytes": 1,
      "realLocationBandwidthLimitInBytes": 1,
      "screenshotCurrentMonthUsage": 1,
      "screenshotLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiAnalysisRequestsCurrentMonthUsage` | number | The AI analysis requests used in the current month. |
| `aiAnalysisRequestsLimit` | number | The AI analysis request limit for the current month. |
| `realLocationBandwidthCurrentMonthUsageInBytes` | number | The real location bandwidth used in the current month in bytes. |
| `realLocationBandwidthLimitInBytes` | number | The monthly real location bandwidth limit in bytes. |
| `screenshotCurrentMonthUsage` | number | The screenshot requests used in the current month. |
| `screenshotLimit` | number | The screenshot request limit for the current month. |

## Native endpoint

Through the native PagePixels API, this operation is `GET /account_limits` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-limits.md) for the provider-specific parameters and requirements.

