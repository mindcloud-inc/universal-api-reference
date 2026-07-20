# Baremetrics: Update Subscription

Updates a subscription in Baremetrics.

```
PUT https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionOid": "subscription_1",
  "sourceId": "source_1",
  "planOid": "plan_1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionOid": "subscription_1",
    "sourceId": "source_1",
    "planOid": "plan_1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionOid` | string | yes | Your unique ID for the subscription Example: `subscription_1`. |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `planOid` | string | yes | Your unique ID for the plan Example: `plan_1`. |
| `occurredAt` | string | no | A unix timestamp of when this change occurred. Defaults to now |
| `addons[]` | array<object> | no | In cents. The OID can be anything you want. |
| `quantity` | number | no |  |
| `discount` | number | no | Integer value (in the same currency as the plan) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `PUT /v1/:source_id/subscriptions/:subscription_oid` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

