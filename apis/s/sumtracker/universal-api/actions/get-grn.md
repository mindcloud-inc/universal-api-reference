# Sumtracker: Get Goods Receipt Note

Retrieves a goods receipt note from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-grn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-grn?connectionId=$CONNECTION_ID&document_type=string&id=string&po_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_type": "string",
  "id": "string",
  "po_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-grn?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | string | yes | Goods receipt note ID. |
| `po_id` | string | yes | Purchase order or stock transfer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": "string",
      "reference": "string",
      "status": "string",
      "actionPerformed": "string",
      "isStockTransfer": true,
      "isTaskInProgress": true,
      "deliveryTime": "2026-05-07T12:00:00.000Z",
      "receiveByTime": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z",
      "totalQuantity": 1,
      "totalAmount": "string",
      "subtotal": "string",
      "totalTax": "string",
      "totalShipping": "string",
      "extraCharges": "string",
      "extraShipping": "string",
      "notes": "string",
      "id": 1,
      "purchaseOrderId": 1,
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `actionPerformed` | string |  |
| `isStockTransfer` | boolean |  |
| `isTaskInProgress` | boolean |  |
| `deliveryTime` | date |  |
| `receiveByTime` | date |  |
| `created` | date |  |
| `updated` | date |  |
| `totalQuantity` | number |  |
| `totalAmount` | string |  |
| `subtotal` | string |  |
| `totalTax` | string |  |
| `totalShipping` | string |  |
| `extraCharges` | string |  |
| `extraShipping` | string |  |
| `notes` | string |  |
| `id` | number |  |
| `purchaseOrderId` | number |  |
| `warehouseId` | number |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/purchases/:document_type/:po_id/grns/:id/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-grn.md) for the provider-specific parameters and requirements.

