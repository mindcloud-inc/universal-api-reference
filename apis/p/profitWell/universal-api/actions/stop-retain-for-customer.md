# ProfitWell: Stop Retain For Customer

Stops Retain interventions for a customer in ProfitWell.

```
POST https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/stop-retain-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/stop-retain-for-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "interventionTypes[]": "reactivation"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/stop-retain-for-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "interventionTypes[]": "reactivation"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The customer ID. |
| `interventionTypes[]` | array<string> | yes | The interventions to stop for the customer. One of: `reactivation`, `retain`, `term_optimization`. |
| `forever` | boolean | no | Whether to exclude the customer from the chosen interventions going forward. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `POST /v2/retain/stop/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-retain-for-customer.md) for the provider-specific parameters and requirements.

