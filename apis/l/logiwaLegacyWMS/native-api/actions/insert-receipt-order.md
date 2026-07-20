# Insert Receipt Order with Logiwa Legacy WMS

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/WarehouseReceiptBulkInsert`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [Insert Receipt Order](https://developer.logiwa.com/?id=5df0dd05e6466c2eec992f69)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `receiptOrders[].Details[].itemCode` | body | `string` | no |
| `receiptOrders[].Details[].itemDescription` | body | `string` | no |
| `receiptOrders[].Details[].ItemPackType` | body | `string` | no |
| `receiptOrders[].Details[].plannedPackQuantity` | body | `number` | no |
| `receiptOrders[].Details[].detailProject` | body | `string` | no |
| `receiptOrders[].Details[].detailQuarantineReason` | body | `string` | no |
| `receiptOrders[].Details[].detailSuitabilityReason` | body | `string` | no |
| `receiptOrders[].Details[].detailPurchaseOrder` | body | `string` | no |
| `receiptOrders[].Details[].detailReceiptCancelReason` | body | `string` | no |
| `receiptOrders[].Details[].palletType` | body | `string` | no |
| `receiptOrders[].Details[].customer` | body | `string` | no |
| `receiptOrders[].Details[].locationCode` | body | `string` | no |
| `receiptOrders[].Details[].expireDate` | body | `date` | no |
| `receiptOrders[].Details[].lotBatchNo` | body | `string` | no |
| `receiptOrders[].Details[].freeAttr1` | body | `string` | no |
| `receiptOrders[].Details[].freeAttr2` | body | `string` | no |
| `receiptOrders[].Details[].freeAttr3` | body | `string` | no |
| `receiptOrders[].Details[].referenceNo` | body | `string` | no |
| `receiptOrders[]` | body | `array` | no |
| `receiptOrders[].addressText` | body | `string` | no |
| `receiptOrders[].addressType` | body | `string` | no |
| `receiptOrders[].backReceiptOrder` | body | `string` | no |
| `receiptOrders[].carrierAddressType` | body | `string` | no |
| `receiptOrders[].city` | body | `string` | no |
| `receiptOrders[].code` | body | `string` | no |
| `receiptOrders[].country` | body | `string` | no |
| `receiptOrders[].currencyCode` | body | `string` | no |
| `receiptOrders[].deliveryNoteNo` | body | `string` | no |
| `receiptOrders[].depositor` | body | `string` | no |
| `receiptOrders[].DepositorRefCode` | body | `string` | no |
| `receiptOrders[].Details[]` | body | `array` | no |
| `receiptOrders[].notes` | body | `string` | no |
| `receiptOrders[].notes2` | body | `string` | no |
| `receiptOrders[].notes3` | body | `string` | no |
| `receiptOrders[].productionOrder` | body | `string` | no |
| `receiptOrders[].project` | body | `string` | no |
| `receiptOrders[].purchaseOrder` | body | `string` | no |
| `receiptOrders[].purchaseOrderType` | body | `string` | no |
| `receiptOrders[].quarantineReason` | body | `string` | no |
| `receiptOrders[].receiptDate` | body | `date` | no |
| `receiptOrders[].receiptMainCategory` | body | `string` | no |
| `receiptOrders[].receiptOrderCancelReason` | body | `string` | no |
| `receiptOrders[].receiptOrderReturnReason` | body | `string` | no |
| `receiptOrders[].salesOrder` | body | `string` | no |
| `receiptOrders[].shipmentOrder` | body | `string` | no |
| `receiptOrders[].state` | body | `string` | no |
| `receiptOrders[].suitabilityReason` | body | `string` | no |
| `receiptOrders[].supplier` | body | `string` | no |
| `receiptOrders[].supplierAddress` | body | `string` | no |
| `receiptOrders[].SupplierRefCode` | body | `string` | no |
| `receiptOrders[].town` | body | `string` | no |
| `receiptOrders[].transportationPaye` | body | `string` | no |
| `receiptOrders[].visitOrder` | body | `string` | no |
| `receiptOrders[].warehouse` | body | `string` | no |
| `receiptOrders[].warehouseReceiptType` | body | `string` | no |
| `receiptOrders[].workOrder` | body | `string` | no |
| `receiptOrders[].zone` | body | `string` | no |
