# CoinMarketCap Universal API Examples

These examples use the MindCloud API key and CoinMarketCap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Key Info

Retrieves API key usage and plan details from CoinMarketCap.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-api-key-info?${params}`, {
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
      "plan": {
        "credit_limit_monthly": 1,
        "credit_limit_monthly_reset": "string",
        "credit_limit_monthly_reset_timestamp": "2026-05-07T12:00:00.000Z",
        "rate_limit_minute": 1
      },
      "usage": {
        "current_day": {
          "credits_used": 1
        },
        "current_minute": {
          "requests_left": 1,
          "requests_made": 1
        },
        "current_month": {
          "credits_left": 1,
          "credits_used": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get API Key Info action reference](actions/get-api-key-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coinMarketCap/latest/actions/get-api-key-info).
