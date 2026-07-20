# ProfitWell: Upgrade Or Downgrade Subscription

Updates a subscription in ProfitWell.

```
PUT https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/upgrade-or-downgrade-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/upgrade-or-downgrade-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionIdOrSubscriptionAlias": "spiderman_sub_1",
  "effectiveDate": "1514764800",
  "planId": "venom_plan",
  "planInterval": "month",
  "value": "7500"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/upgrade-or-downgrade-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionIdOrSubscriptionAlias": "spiderman_sub_1",
    "effectiveDate": "1514764800",
    "planId": "venom_plan",
    "planInterval": "month",
    "value": "7500"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionIdOrSubscriptionAlias` | string | yes | Either the subscription_id or the subscription_alias of the subscription. Example: `spiderman_sub_1`. |
| `effectiveDate` | number | yes | The date that this update takes effect, in UNIX timestamp format. Example: `1514764800`. |
| `planId` | string | yes | The ID of the plan that the user is switching to. Example: `venom_plan`. |
| `planInterval` | string | yes | The billing cycle for this plan. The two options are month and year. Example: `month`. |
| `status` | string | no | The only valid status when upgrading or downgrading a subscription is active. Default: `active`. Example: `active`. |
| `value` | number | yes | The new amount that you bill your user, per billing period, in cents. Example: `7500`. |

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

Through the native ProfitWell API, this operation is `PUT /v2/subscriptions/:subscriptionIdOrSubscriptionAlias/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upgrade-or-downgrade-subscription.md) for the provider-specific parameters and requirements.

