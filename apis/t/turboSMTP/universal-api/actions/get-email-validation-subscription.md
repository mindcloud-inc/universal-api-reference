# turboSMTP: Get Email Validation Subscription

Retrieves email validation subscription details from turboSMTP.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-email-validation-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-email-validation-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-email-validation-subscription?${params}`, {
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
      "currency": "string",
      "free_credits": 1,
      "free_credits_used": 1,
      "last_used_period": "string",
      "latest_period_start_date": "string",
      "paid_credits": 1,
      "period_expiration_date": "string",
      "remaining_free_credit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `free_credits` | number |  |
| `free_credits_used` | number |  |
| `last_used_period` | string |  |
| `latest_period_start_date` | string |  |
| `paid_credits` | number |  |
| `period_expiration_date` | string |  |
| `remaining_free_credit` | number |  |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /emailvalidation/subscription` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-validation-subscription.md) for the provider-specific parameters and requirements.

