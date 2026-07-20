# Baremetrics: Create Subscription

Creates a subscription in Baremetrics.

```
POST https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "source_1",
  "oid": "resource_1",
  "startedAt": "string",
  "planOid": "plan_1",
  "customerOid": "customer_1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "source_1",
    "oid": "resource_1",
    "startedAt": "string",
    "planOid": "plan_1",
    "customerOid": "customer_1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `oid` | string | yes | Your unique ID for the subscription Example: `resource_1`. |
| `startedAt` | string | yes | A unix timestamp of when this subscription started |
| `canceledAt` | string | no | A unix timestamp of when this subscription was, or should be canceled. This cannot be changed, so only set this if you are certain you know when the subscription will end. |
| `planOid` | string | yes | Your unique ID for the plan Example: `plan_1`. |
| `customerOid` | string | yes | Your unique ID for the customer Example: `customer_1`. |
| `addons[]` | array<object> | no |  |
| `quantity` | number | no |  |
| `discount` | number | no | Integer value (in the same currency as the plan) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `POST /v1/:source_id/subscriptions` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

