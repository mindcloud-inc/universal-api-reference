# inFlow Inventory: Get Product Inventory Summary

Retrieves a product inventory summary from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-product-inventory-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-product-inventory-summary?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-product-inventory-summary?${params}`, {
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
| `productId` | string | yes | The inFlow product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "imageSmallUrl": "https://example.com",
      "locationId": "string",
      "productId": "string",
      "quantityAnticipated": "string",
      "quantityAvailable": "string",
      "quantityBuildable": "string",
      "quantityExpiring": "string",
      "quantityInTransit": "string",
      "quantityOnHand": "string",
      "quantityOnOrder": "string",
      "quantityOnPurchaseOrder": "string",
      "quantityOnTransferOrder": "string",
      "quantityOnWorkOrder": "string",
      "quantityPicked": "string",
      "quantityReserved": "string",
      "quantityReservedForBuilds": "string",
      "quantityReservedForManufacturing": "string",
      "quantityReservedForSales": "string",
      "quantityReservedForTransfers": "string",
      "rawQuantityAvailable": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `imageSmallUrl` | string |  |
| `locationId` | string |  |
| `productId` | string |  |
| `quantityAnticipated` | string |  |
| `quantityAvailable` | string |  |
| `quantityBuildable` | string |  |
| `quantityExpiring` | string |  |
| `quantityInTransit` | string |  |
| `quantityOnHand` | string |  |
| `quantityOnOrder` | string |  |
| `quantityOnPurchaseOrder` | string |  |
| `quantityOnTransferOrder` | string |  |
| `quantityOnWorkOrder` | string |  |
| `quantityPicked` | string |  |
| `quantityReserved` | string |  |
| `quantityReservedForBuilds` | string |  |
| `quantityReservedForManufacturing` | string |  |
| `quantityReservedForSales` | string |  |
| `quantityReservedForTransfers` | string |  |
| `rawQuantityAvailable` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /products/:productId/summary` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-inventory-summary.md) for the provider-specific parameters and requirements.

