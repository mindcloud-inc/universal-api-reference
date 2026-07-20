# Sumtracker: Create Goods Receipt Note Line

Creates a goods receipt note line in Sumtracker.

```
POST https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-grn-line
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-grn-line" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document_type": "string",
  "grn_id": "string",
  "po_id": "string",
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-grn-line', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document_type": "string",
    "grn_id": "string",
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
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `grn_id` | string | yes | Goods receipt note ID. |
| `po_id` | string | yes | Purchase order or stock transfer ID. |
| `poline_id` | number | no |  |
| `quantity` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumtracker API returns.

## Native endpoint

Through the native Sumtracker API, this operation is `POST /api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-grn-line.md) for the provider-specific parameters and requirements.

