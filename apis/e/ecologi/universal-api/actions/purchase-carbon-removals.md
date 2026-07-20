# Ecologi: Purchase Carbon Removals

Purchases carbon removals through Ecologi.

```
POST https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-carbon-removals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecologi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-carbon-removals" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-carbon-removals', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | number | yes | The number of kilograms of carbon removal to purchase. Example: `10`. |
| `name` | string | no | Optional funded-by name shown with the purchase. Example: `Our valued customer 'X' for order 'Y'`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `test` | boolean | no | Optional advanced flag retained for Ecologi purchase requests. Current public Ecologi guidance does not clearly document sandbox semantics, and runtime validation still required billing details with this flag enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecologi API returns.

## Native endpoint

Through the native Ecologi API, this operation is `POST /impact/carbon-removal` (base URL `https://public.ecologi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-carbon-removals.md) for the provider-specific parameters and requirements.

