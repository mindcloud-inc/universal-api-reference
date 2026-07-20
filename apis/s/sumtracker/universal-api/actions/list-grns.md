# Sumtracker: List Goods Receipt Notes

Retrieves goods receipt notes from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-grns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-grns?connectionId=$CONNECTION_ID&limit=25&offset=0&document_type=string&po_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "document_type": "string",
  "po_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-grns?${params}`, {
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
| `po_id` | string | yes | Purchase order or stock transfer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
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
      "count": 1,
      "next": "string",
      "previous": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].number` | string |  |
| `results[].reference` | string |  |
| `results[].status` | string |  |
| `results[].actionPerformed` | string |  |
| `results[].isStockTransfer` | boolean |  |
| `results[].isTaskInProgress` | boolean |  |
| `results[].deliveryTime` | date |  |
| `results[].receiveByTime` | date |  |
| `results[].created` | date |  |
| `results[].updated` | date |  |
| `results[].totalQuantity` | number |  |
| `results[].totalAmount` | string |  |
| `results[].subtotal` | string |  |
| `results[].totalTax` | string |  |
| `results[].totalShipping` | string |  |
| `results[].extraCharges` | string |  |
| `results[].extraShipping` | string |  |
| `results[].notes` | string |  |
| `results[].id` | number |  |
| `results[].purchaseOrderId` | number |  |
| `results[].warehouseId` | number |  |
| `count` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/purchases/:document_type/:po_id/grns/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-grns.md) for the provider-specific parameters and requirements.

