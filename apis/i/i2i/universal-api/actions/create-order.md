# i2i: Create order

Creates a new ship order in i2i.

```
POST https://connect.mindcloud.co/v1/universal/i2i/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a i2i `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/i2i/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "header": {},
  "lines[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/i2i/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "header": {},
    "lines[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `header` | object | yes | Order header object matching the existing i2i connector payload: number, ref_no, po_no, service, shipper, soldto, shipto, and optional comments. |
| `lines[]` | array<object> | yes | Line item array matching the existing i2i connector payload. Each line includes description, item, and qty. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native i2i API returns.

## Native endpoint

Through the native i2i API, this operation is `POST /ibis/api/v1.1/customers/{{credentials.consumerTag}}/ship/orders` (base URL `https://exch.i2i.ca`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

