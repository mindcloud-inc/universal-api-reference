# Routee: Detailed balance info

Retrieves detailed balance information from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/detailed-balance-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/detailed-balance-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/detailed-balance-info?${params}`, {
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
        "emails_left": 1,
        "finished_time": "ava@example.com",
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
        "end_date": "string",
        "tariff_name": "Ava Chen"
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
| `email.emails_left` | number |  |
| `email.finished_time` | string |  |
| `email.maximum_subscribers` | number |  |
| `email.tariff_name` | string |  |
| `push` | object |  |
| `push.auto_renew` | number |  |
| `push.end_date` | string |  |
| `push.tariff_name` | string |  |
| `smtp` | object |  |
| `smtp.auto_renew` | number |  |
| `smtp.end_date` | string |  |
| `smtp.tariff_name` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /user/balance/detail` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detailed-balance-info.md) for the provider-specific parameters and requirements.

