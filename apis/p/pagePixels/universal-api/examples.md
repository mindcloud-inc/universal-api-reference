# PagePixels Universal API Examples

These examples use the MindCloud API key and PagePixels connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Limits



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

Example response:

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

See the full [Get Account Limits action reference](actions/get-account-limits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pagePixels/latest/actions/get-account-limits).

## Capture Next Scheduled Screenshot



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/capture-next-scheduled-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "screenshotConfigurationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/capture-next-scheduled-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "screenshotConfigurationId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "embedUrl": "https://example.com",
      "jobId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Capture Next Scheduled Screenshot action reference](actions/capture-next-scheduled-screenshot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pagePixels/latest/actions/capture-next-scheduled-screenshot).
