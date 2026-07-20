# ProfitWell: Churn Subscription

Churns a subscription in ProfitWell.

```
DELETE https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/churn-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/churn-subscription?connectionId=$CONNECTION_ID&subscriptionIdOrSubscriptionAlias=spiderman_sub_1&effectiveDate=1514764800" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionIdOrSubscriptionAlias": "spiderman_sub_1",
  "effectiveDate": "1514764800"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/churn-subscription?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionIdOrSubscriptionAlias` | string | yes | Either the subscription_id or the subscription_alias of the subscription. Example: `spiderman_sub_1`. |
| `effectiveDate` | number | yes | UNIX timestamp of when the subscription churns. Example: `1514764800`. |
| `churnType` | string | no | Acceptable values are voluntary or delinquent. Default: `voluntary`. Example: `voluntary`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "effective_date": 1,
      "email": "ava@example.com",
      "meta": {},
      "plan_currency": "string",
      "plan_id": "string",
      "plan_interval": "string",
      "status": "string",
      "subscription_alias": "string",
      "subscription_id": "string",
      "user_alias": "string",
      "user_id": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effective_date` | number |  |
| `email` | string |  |
| `meta` | object |  |
| `plan_currency` | string |  |
| `plan_id` | string |  |
| `plan_interval` | string |  |
| `status` | string |  |
| `subscription_alias` | string |  |
| `subscription_id` | string |  |
| `user_alias` | string |  |
| `user_id` | string |  |
| `value` | number |  |

## Native endpoint

Through the native ProfitWell API, this operation is `DELETE /v2/subscriptions/:subscriptionIdOrSubscriptionAlias/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/churn-subscription.md) for the provider-specific parameters and requirements.

