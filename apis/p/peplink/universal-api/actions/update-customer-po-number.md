# Peplink: Update customer PO number

Update customer PO number for an order.

```
POST https://connect.mindcloud.co/v1/universal/peplink/latest/actions/update-customer-po-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peplink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peplink/latest/actions/update-customer-po-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderNumber": "string",
  "customerPoNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peplink/latest/actions/update-customer-po-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderNumber": "string",
    "customerPoNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderNumber` | string | yes |  |
| `customerPoNumber` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Peplink API returns.

## Native endpoint

Through the native Peplink API, this operation is `POST /orders/:orderNumber/customer-po-number` (base URL `https://portal.peplink.com/api/e/v1/cp/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-po-number.md) for the provider-specific parameters and requirements.

