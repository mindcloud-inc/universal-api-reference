# Boomlify: Get Account Usage

Retrieves API usage statistics from Boomlify.

```
GET https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-usage?${params}`, {
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
      "account": {
        "email": "ava@example.com",
        "tier": "string"
      },
      "credit_info": {
        "available_credits": 1,
        "paid_balance": 1,
        "tier": "string"
      },
      "meta": {
        "request_time": "2026-05-07T12:00:00.000Z"
      },
      "success": true,
      "usage_stats": {
        "history": [
          {}
        ],
        "summary": {
          "total_credits_used": 1,
          "total_emails_created": 1
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
| `account` | object |  |
| `account.email` | string |  |
| `account.tier` | string |  |
| `credit_info` | object |  |
| `credit_info.available_credits` | number |  |
| `credit_info.paid_balance` | number |  |
| `credit_info.tier` | string |  |
| `meta` | object |  |
| `meta.request_time` | date |  |
| `success` | boolean |  |
| `usage_stats` | object |  |
| `usage_stats.history` | array<object> |  |
| `usage_stats.summary` | object |  |
| `usage_stats.summary.total_credits_used` | number |  |
| `usage_stats.summary.total_emails_created` | number |  |

## Native endpoint

Through the native Boomlify API, this operation is `GET /api/v1/account/usage` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-usage.md) for the provider-specific parameters and requirements.

