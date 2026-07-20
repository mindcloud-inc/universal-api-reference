# Fiddle: Find Purchase Order by ID

Finds a purchase order in Fiddle by ID.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/find-purchase-order-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/find-purchase-order-by-id?connectionId=$CONNECTION_ID&purchaseOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/find-purchase-order-by-id?${params}`, {
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
| `purchaseOrderId` | string | yes | Purchase order ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "purchaseOrder": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "notes": "string",
        "purchaseOrderNumber": "string",
        "status": "string",
        "supplier": {
          "id": "string",
          "name": "Ava Chen"
        },
        "supplierId": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `purchaseOrder` | object |  |
| `purchaseOrder.createdAt` | date |  |
| `purchaseOrder.id` | string |  |
| `purchaseOrder.notes` | string |  |
| `purchaseOrder.purchaseOrderNumber` | string |  |
| `purchaseOrder.status` | string |  |
| `purchaseOrder.supplier` | object |  |
| `purchaseOrder.supplier.id` | string |  |
| `purchaseOrder.supplier.name` | string |  |
| `purchaseOrder.supplierId` | string |  |
| `purchaseOrder.updatedAt` | date |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /purchase-orders/:purchaseOrderId` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-purchase-order-by-id.md) for the provider-specific parameters and requirements.

