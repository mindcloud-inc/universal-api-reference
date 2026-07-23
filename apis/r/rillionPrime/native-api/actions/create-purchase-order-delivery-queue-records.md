# Create Purchase Order Delivery Queue Records with Rillion Prime

## Endpoint

- **Method:** `PUT`
- **Path:** `/purchaseorderdeliveryqueue`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Purchase Order Delivery Queue Records](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Buyer%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderDeliveries[]` | body | `array<object>` | no | Request body value for PurchaseOrderDeliveries. |
| `purchaseOrderDeliveries[].company` | body | `string` | no | — |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].purchaseOrderNo` | body | `string` | no | — |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].lineNo` | body | `string` | no | — |
| `purchaseOrderDeliveries[].supplier` | body | `string` | no | — |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].number` | body | `number` | no | — |
| `purchaseOrderDeliveries[].supplierDeliveryNote` | body | `string` | no | — |
| `purchaseOrderDeliveries[].deliveryNote` | body | `string` | no | — |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].amount` | body | `number` | no | — |
| `purchaseOrderDeliveries[].deliveryDate` | body | `string` | no | — |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].queueStatus` | body | `number` | no | — |
| `purchaseOrderDeliveries[].queueStatus` | body | `number` | no | — |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[]` | body | `array<object>` | no | — |
