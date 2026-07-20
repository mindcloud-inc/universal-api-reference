# Logiwa Legacy WMS: List Shipment Orders



```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-shipment-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-shipment-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-shipment-orders?${params}`, {
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
| `iD` | string | no |  |
| `code` | string | no |  |
| `priorityID` | string | no |  |
| `customerRefCode` | string | no |  |
| `depositorRefCode` | string | no |  |
| `customerOrderNo` | string | no |  |
| `depositorOrderNo` | string | no |  |
| `warehouseOrderStatusID` | string | no |  |
| `customerID` | number | no |  |
| `customerCode` | string | no |  |
| `customerDescription` | string | no |  |
| `inventorySiteID` | string | no |  |
| `inventorySiteCode` | string | no |  |
| `warehouseID` | number | no |  |
| `warehouseCode` | string | no |  |
| `warehouseDescription` | string | no |  |
| `depositorID` | number | no |  |
| `depositorCode` | string | no |  |
| `depositorDescription` | string | no |  |
| `isPrintCarrierLabelPackListAsLabel` | boolean | no |  |
| `carrierTrackingNumber` | string | no |  |
| `orderDate` | string | no |  |
| `plannedDeliveryDateStart` | string | no |  |
| `plannedDeliveryDateEnd` | string | no |  |
| `plannedShipDateStart` | string | no |  |
| `plannedShipDateEnd` | string | no |  |
| `lastModifiedDateStart` | string | no |  |
| `lastModifiedDateEnd` | string | no |  |
| `notes` | string | no |  |
| `businessDaysInTransit` | string | no |  |
| `customerEmail` | string | no |  |
| `isPrintCarrierLabelPackListOnSamePage` | boolean | no |  |
| `warehouseOrderTypeID` | string | no |  |
| `warehouseOrderTypeCode` | string | no |  |
| `cancellationDateStart` | string | no |  |
| `cancellationDateEnd` | string | no |  |
| `isDocumentExist` | boolean | no |  |
| `purchaseOrderID` | string | no |  |
| `purchaseOrderCode` | string | no |  |
| `isBackorder` | boolean | no |  |
| `nofShipmentLabel` | string | no |  |
| `isAllocated` | boolean | no |  |
| `isPickingStarted` | boolean | no |  |
| `isPickingCompleted` | boolean | no |  |
| `channelID` | string | no |  |
| `channelDescription` | string | no |  |
| `carrierID` | string | no |  |
| `carrierDescription` | string | no |  |
| `carrierShippingOptionsID` | string | no |  |
| `nofProducts` | string | no |  |
| `storeName` | string | no |  |
| `linkedChannelID` | string | no |  |
| `linkedChannelDescription` | string | no |  |
| `backWarehouseOrderID` | string | no |  |
| `backWarehouseOrderCode` | string | no |  |
| `dropShipMasterOrderID` | string | no |  |
| `dropShipWarehouseOrderCode` | string | no |  |
| `dropShipNotes` | string | no |  |
| `channelOrderCode` | string | no |  |
| `warehouseOrderOperationStatus` | string | no |  |
| `carrierBillingTypeID` | string | no |  |
| `carrierBillingTypeDescription` | string | no |  |
| `driver` | string | no |  |
| `taxesandDutiesBillingType` | string | no |  |
| `taxandDutiesPayorInfo` | string | no |  |
| `methodName` | list<string> | no |  |
| `isGetOrderDetails` | boolean | no | Default: `true`. |
| `isGetCustomerAddressInfo` | boolean | no | Default: `True`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/WarehouseOrderSearch` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shipment-orders.md) for the provider-specific parameters and requirements.

