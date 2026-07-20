# Logiwa Legacy WMS: Update Receipt Order Detail

By using this endpoint, users can UPDATE the details of receipt orders if the ID field exists in the endpoint request. 

Users can CREATE receipt order details unless the Warehouse Receipt Order Detail ID is not added to the request.

```
POST https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/update-receipt-order-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/update-receipt-order-detail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inventoryItemID": 1,
  "inventoryItemPackTypeID": 1,
  "plannedCUQuantity": 1,
  "plannedPackQuantity": 1,
  "warehouseReceiptID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/update-receipt-order-detail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inventoryItemID": 1,
    "inventoryItemPackTypeID": 1,
    "plannedCUQuantity": 1,
    "plannedPackQuantity": 1,
    "warehouseReceiptID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | no |  |
| `expireDate` | string | no |  |
| `freeAttr1` | string | no |  |
| `freeAttr2` | string | no |  |
| `freeAttr3` | string | no |  |
| `iD` | number | no |  |
| `inventoryItemID` | number | yes |  |
| `inventoryItemPackTypeDescription` | string | no |  |
| `inventoryItemPackTypeID` | number | yes |  |
| `lotBatchNo` | string | no |  |
| `notes2` | string | no |  |
| `plannedCUQuantity` | number | yes |  |
| `plannedPackQuantity` | number | yes |  |
| `productionDate` | string | no |  |
| `sSCC` | string | no |  |
| `warehouseReceiptID` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/WarehouseReceiptDetailUpdate` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-receipt-order-detail.md) for the provider-specific parameters and requirements.

