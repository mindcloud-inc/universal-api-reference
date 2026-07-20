# Sumtracker: Create Purchase Order Line

Creates a purchase order line in Sumtracker.

```
POST https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-po-line
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-po-line" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document_type": "string",
  "po_id": "string",
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-po-line', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document_type": "string",
    "po_id": "string",
    "quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cost` | number | no |  |
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `notes` | string | no |  |
| `po_id` | string | yes | Purchase order or stock transfer ID. |
| `product` | number | no |  |
| `quantity` | number | yes |  |
| `tax_id` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumtracker API returns.

## Native endpoint

Through the native Sumtracker API, this operation is `POST /api/version/2025-03/purchases/:document_type/:po_id/lines/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-po-line.md) for the provider-specific parameters and requirements.

