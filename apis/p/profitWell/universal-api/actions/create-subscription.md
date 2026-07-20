# ProfitWell: Create Subscription

Creates a subscription in ProfitWell.

```
POST https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "spiderman@profitwell.com",
  "planId": "web_plan",
  "planInterval": "month",
  "value": "5000",
  "effectiveDate": "1514764800"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "spiderman@profitwell.com",
    "planId": "web_plan",
    "planInterval": "month",
    "value": "5000",
    "effectiveDate": "1514764800"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userAlias` | string | no | Your own identifier for this user so that you have a handle by which to refer to this user in subsequent requests. Example: `spiderman`. |
| `subscriptionAlias` | string | no | Your own identifier for this subscription. Must be unique across all users in your company. Example: `spiderman_sub_1`. |
| `email` | string | yes | The email address of the user. Example: `spiderman@profitwell.com`. |
| `planId` | string | yes | The ID of the plan that the user is on. Example: `web_plan`. |
| `planInterval` | string | yes | The billing cycle for this plan. The two options are month and year. Example: `month`. |
| `planCurrency` | string | no | The currency in which users of this plan are charged. Default: `usd`. Example: `usd`. |
| `status` | string | no | The status of the subscription. Acceptable values for new subscriptions are active and trialing. Default: `active`. Example: `active`. |
| `value` | number | yes | The amount that you bill your user, per billing period, in cents. Example: `5000`. |
| `effectiveDate` | number | yes | The date that the subscription starts, in UNIX timestamp format. Example: `1514764800`. |

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

Through the native ProfitWell API, this operation is `POST /v2/subscriptions/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

