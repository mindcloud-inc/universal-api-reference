# Logiwa Legacy WMS: Insert Receipt Order



```
POST https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-receipt-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-receipt-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-receipt-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `receiptOrders[].details[].itemCode` | string | no |  |
| `receiptOrders[].details[].itemDescription` | string | no |  |
| `receiptOrders[].details[].itemPackType` | string | no |  |
| `receiptOrders[].details[].plannedPackQuantity` | number | no |  |
| `receiptOrders[].details[].detailProject` | string | no |  |
| `receiptOrders[].details[].detailQuarantineReason` | string | no |  |
| `receiptOrders[].details[].detailSuitabilityReason` | string | no |  |
| `receiptOrders[].details[].detailPurchaseOrder` | string | no |  |
| `receiptOrders[].details[].detailReceiptCancelReason` | string | no |  |
| `receiptOrders[].details[].palletType` | string | no |  |
| `receiptOrders[].details[].customer` | string | no |  |
| `receiptOrders[].details[].locationCode` | string | no |  |
| `receiptOrders[].details[].expireDate` | date | no |  |
| `receiptOrders[].details[].lotBatchNo` | string | no |  |
| `receiptOrders[].details[].freeAttr1` | string | no |  |
| `receiptOrders[].details[].freeAttr2` | string | no |  |
| `receiptOrders[].details[].freeAttr3` | string | no |  |
| `receiptOrders[].details[].referenceNo` | string | no |  |
| `receiptOrders[]` | array | no |  |
| `receiptOrders[].addressText` | string | no |  |
| `receiptOrders[].addressType` | string | no |  |
| `receiptOrders[].backReceiptOrder` | string | no |  |
| `receiptOrders[].carrierAddressType` | string | no |  |
| `receiptOrders[].city` | string | no |  |
| `receiptOrders[].code` | string | no |  |
| `receiptOrders[].country` | string | no |  |
| `receiptOrders[].currencyCode` | string | no |  |
| `receiptOrders[].deliveryNoteNo` | string | no |  |
| `receiptOrders[].depositor` | string | no |  |
| `receiptOrders[].depositorRefCode` | string | no |  |
| `receiptOrders[].details[]` | array | no |  |
| `receiptOrders[].notes` | string | no |  |
| `receiptOrders[].notes2` | string | no |  |
| `receiptOrders[].notes3` | string | no |  |
| `receiptOrders[].productionOrder` | string | no |  |
| `receiptOrders[].project` | string | no |  |
| `receiptOrders[].purchaseOrder` | string | no |  |
| `receiptOrders[].purchaseOrderType` | string | no |  |
| `receiptOrders[].quarantineReason` | string | no |  |
| `receiptOrders[].receiptDate` | date | no |  |
| `receiptOrders[].receiptMainCategory` | string | no |  |
| `receiptOrders[].receiptOrderCancelReason` | string | no |  |
| `receiptOrders[].receiptOrderReturnReason` | string | no |  |
| `receiptOrders[].salesOrder` | string | no |  |
| `receiptOrders[].shipmentOrder` | string | no |  |
| `receiptOrders[].state` | string | no |  |
| `receiptOrders[].suitabilityReason` | string | no |  |
| `receiptOrders[].supplier` | string | no |  |
| `receiptOrders[].supplierAddress` | string | no |  |
| `receiptOrders[].supplierRefCode` | string | no |  |
| `receiptOrders[].town` | string | no |  |
| `receiptOrders[].transportationPaye` | string | no |  |
| `receiptOrders[].visitOrder` | string | no |  |
| `receiptOrders[].warehouse` | string | no |  |
| `receiptOrders[].warehouseReceiptType` | string | no |  |
| `receiptOrders[].workOrder` | string | no |  |
| `receiptOrders[].zone` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/WarehouseReceiptBulkInsert` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-receipt-order.md) for the provider-specific parameters and requirements.

