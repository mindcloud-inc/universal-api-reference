# TypeCast: Get Subscription

Retrieves current subscription details from TypeCast.

```
GET https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TypeCast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeCast/latest/actions/get-subscription?${params}`, {
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
      "credits": {
        "planCredits": 1,
        "usedCredits": 1
      },
      "limits": {
        "concurrencyLimit": 1
      },
      "plan": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits.planCredits` | number | Total monthly credits provided by the plan. |
| `credits.usedCredits` | number | Number of credits used. |
| `limits.concurrencyLimit` | number | Maximum number of concurrent requests allowed. |
| `plan` | string | Current subscription plan. |

## Native endpoint

Through the native TypeCast API, this operation is `GET /v1/users/me/subscription` (base URL `https://api.typecast.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

