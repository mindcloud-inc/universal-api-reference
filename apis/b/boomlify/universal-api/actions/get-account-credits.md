# Boomlify: Get Account Credits

Retrieves credit balance and usage information from Boomlify.

```
GET https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-credits?${params}`, {
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
      "conversion": {
        "credits_per_usd": 1,
        "usd_per_credit": "string"
      },
      "credits": {
        "costs_per_email": {},
        "current_balance": 1,
        "usd_equivalent": "string"
      },
      "meta": {
        "request_time": "2026-05-07T12:00:00.000Z",
        "user_id": "string"
      },
      "success": true,
      "usage_stats": {
        "period_days": 1,
        "recent_transactions": [
          {}
        ],
        "total_earned": 1,
        "total_spent": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversion` | object |  |
| `conversion.credits_per_usd` | number |  |
| `conversion.usd_per_credit` | string |  |
| `credits` | object |  |
| `credits.costs_per_email` | object |  |
| `credits.current_balance` | number |  |
| `credits.usd_equivalent` | string |  |
| `meta` | object |  |
| `meta.request_time` | date |  |
| `meta.user_id` | string |  |
| `success` | boolean |  |
| `usage_stats` | object |  |
| `usage_stats.period_days` | number |  |
| `usage_stats.recent_transactions` | array<object> |  |
| `usage_stats.total_earned` | number |  |
| `usage_stats.total_spent` | number |  |

## Native endpoint

Through the native Boomlify API, this operation is `GET /api/v1/account/credits` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-credits.md) for the provider-specific parameters and requirements.

