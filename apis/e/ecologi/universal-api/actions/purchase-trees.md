# Ecologi: Purchase Trees

Purchases trees through Ecologi.

```
POST https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-trees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecologi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-trees" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-trees', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | number | yes | The number of trees to purchase. Example: `2`. |
| `name` | string | no | Optional funded-by name shown with the purchased trees. Example: `Our valued customer 'X' for order 'Y'`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `test` | boolean | no | Optional advanced flag retained for Ecologi purchase requests. Current public Ecologi guidance does not clearly document sandbox semantics, and runtime validation still required billing details with this flag enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecologi API returns.

## Native endpoint

Through the native Ecologi API, this operation is `POST /impact/trees` (base URL `https://public.ecologi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-trees.md) for the provider-specific parameters and requirements.

