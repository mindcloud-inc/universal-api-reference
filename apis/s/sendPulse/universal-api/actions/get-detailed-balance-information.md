# SendPulse: Get Detailed Balance Information

Retrieves detailed account balance information from SendPulse.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-detailed-balance-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-detailed-balance-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-detailed-balance-information?${params}`, {
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
      "balance": {
        "bonus": "string",
        "currency": "string",
        "main": "string"
      },
      "email": {
        "current_subscribers": 1,
        "finished_time": "ava@example.com",
        "is_unique_type": true,
        "maximum_subscribers": 1,
        "tariff_name": "ava@example.com"
      },
      "push": {
        "auto_renew": 1,
        "end_date": "string",
        "tariff_name": "Ava Chen"
      },
      "smtp": {
        "auto_renew": 1,
        "email_qty": 1,
        "email_qty_left": 1,
        "end_date": "string",
        "qty_per_hour": 1,
        "tariff_name": "Ava Chen",
        "traffic_limit": "string",
        "traffic_limit_left": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | object |  |
| `balance.bonus` | string |  |
| `balance.currency` | string |  |
| `balance.main` | string |  |
| `email` | object |  |
| `email.current_subscribers` | number |  |
| `email.finished_time` | string |  |
| `email.is_unique_type` | boolean |  |
| `email.maximum_subscribers` | number |  |
| `email.tariff_name` | string |  |
| `push` | object |  |
| `push.auto_renew` | number |  |
| `push.end_date` | string |  |
| `push.tariff_name` | string |  |
| `smtp` | object |  |
| `smtp.auto_renew` | number |  |
| `smtp.email_qty` | number |  |
| `smtp.email_qty_left` | number |  |
| `smtp.end_date` | string |  |
| `smtp.qty_per_hour` | number |  |
| `smtp.tariff_name` | string |  |
| `smtp.traffic_limit` | string |  |
| `smtp.traffic_limit_left` | string |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /user/balance/detail` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-detailed-balance-information.md) for the provider-specific parameters and requirements.

