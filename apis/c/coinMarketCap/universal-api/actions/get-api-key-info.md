# CoinMarketCap: Get API Key Info

Retrieves API key usage and plan details from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-api-key-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plan.credit_limit_monthly` | number |  |
| `plan.credit_limit_monthly_reset` | string |  |
| `plan.credit_limit_monthly_reset_timestamp` | date |  |
| `plan.rate_limit_minute` | number |  |
| `usage.current_day.credits_used` | number |  |
| `usage.current_minute.requests_left` | number |  |
| `usage.current_minute.requests_made` | number |  |
| `usage.current_month.credits_left` | number |  |
| `usage.current_month.credits_used` | number |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v1/key/info` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key-info.md) for the provider-specific parameters and requirements.

