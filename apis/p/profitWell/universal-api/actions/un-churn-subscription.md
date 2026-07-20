# ProfitWell: Un-Churn Subscription

Reactivates a churned subscription in ProfitWell.

```
PUT https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/un-churn-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/un-churn-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionIdOrSubscriptionAlias": "spiderman_sub_1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/un-churn-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionIdOrSubscriptionAlias": "spiderman_sub_1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionIdOrSubscriptionAlias` | string | yes | Either the subscription_id or the subscription_alias of the subscription you would like to un-churn. Example: `spiderman_sub_1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `PUT /v2/unchurn/:subscriptionIdOrSubscriptionAlias/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/un-churn-subscription.md) for the provider-specific parameters and requirements.

