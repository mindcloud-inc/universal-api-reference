# Logiwa Legacy WMS: Insert Shipment Order



```
POST https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-shipment-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-shipment-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "methodName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-shipment-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "methodName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipmentOrders[].code` | string | no |  |
| `shipmentOrders[].details[].itemCode` | string | no |  |
| `methodName` | list<string> | yes | ***InsertShipmentOrder Endpoint***: - Lists the orders as a group and if one of the orders fails to import, the whole request operations will be rolled back and none of the orders will be imported ***InsertShipmentOrderWithBulkResult***: - Evaluates orders separately. The successful records will be created and the failed records will be listed with an error message in the response. |
| `shipmentOrders[].depositor` | string | no |  |
| `shipmentOrders[].details[].itemPackType` | string | no |  |
| `shipmentOrders[].details[].plannedPackQuantity` | string | no | Planned quantity per defined pack type |
| `shipmentOrders[].warehouseOrderStatus` | string | no |  |
| `shipmentOrders[].details[].notes` | string | no |  |
| `shipmentOrders[].inventorySite` | string | no |  |
| `shipmentOrders[].details[].location` | string | no |  |
| `shipmentOrders[].warehouse` | string | no |  |
| `shipmentOrders[].details[].lotBatchNo` | string | no |  |
| `shipmentOrders[].warehouseOrderType` | string | no |  |
| `shipmentOrders[].customer` | string | no |  |
| `shipmentOrders[].details[].giftNote` | string | no |  |
| `shipmentOrders[].customerAddress` | string | no |  |
| `shipmentOrders[].details[].freeAttr1` | string | no |  |
| `shipmentOrders[].details[].freeAttr2` | string | no |  |
| `shipmentOrders[].OrderDate` | string | no |  |
| `shipmentOrders[].details[].freeAttr3` | string | no |  |
| `shipmentOrders[].state` | string | no |  |
| `shipmentOrders[].country` | string | no |  |
| `shipmentOrders[].details[].notes1` | string | no |  |
| `shipmentOrders[].city` | string | no |  |
| `shipmentOrders[].details[].notes2` | string | no |  |
| `shipmentOrders[].details[].notes3` | string | no |  |
| `shipmentOrders[].postalCode` | string | no |  |
| `shipmentOrders[].details[].channelorderdetailcode` | string | no |  |
| `shipmentOrders[].phone` | string | no |  |
| `shipmentOrders[].details[].detailEDIReferences` | string | no |  |
| `shipmentOrders[].email` | string | no |  |
| `shipmentOrders[].adressText` | string | no |  |
| `shipmentOrders[].details[].salesUnitPrice` | string | no |  |
| `shipmentOrders[].partyAdressType` | string | no |  |
| `shipmentOrders[].eDIBillTo` | string | no |  |
| `shipmentOrders[].businessDaysInTransit` | number | no |  |
| `shipmentOrders[].isCheckAllocationAvailability` | boolean | no |  |
| `shipmentOrders[].carrier` | string | no |  |
| `shipmentOrders[].prefix` | string | no |  |
| `shipmentOrders[].driver` | string | no |  |
| `shipmentOrders[].plannedShipDate` | string | no |  |
| `shipmentOrders[].earliestShipDate` | string | no |  |
| `shipmentOrders[].latestShipDate` | string | no |  |
| `shipmentOrders[].earliestDeliveryDate` | string | no |  |
| `shipmentOrders[].latestDeliveryDate` | string | no |  |
| `shipmentOrders[].warehouseReceipt` | string | no |  |
| `shipmentOrders[].notes` | string | no |  |
| `shipmentOrders[].customeRefCode` | string | no |  |
| `shipmentOrders[].depositorRefCode` | string | no |  |
| `shipmentOrders[].customerOrderNo` | string | no |  |
| `shipmentOrders[].giftNote` | string | no |  |
| `shipmentOrders[].deliveryNoteNo` | string | no |  |
| `shipmentOrders[].extraNotes` | string | no |  |
| `shipmentOrders[].instructions` | string | no |  |
| `shipmentOrders[].extraNotes1` | string | no |  |
| `shipmentOrders[].extraNotes1` | string | no |  |
| `shipmentOrders[].extraNotes3` | string | no |  |
| `shipmentOrders[].extraNotes4` | string | no |  |
| `shipmentOrders[].extraNotes5` | string | no |  |
| `shipmentOrders[].channel` | string | no |  |
| `shipmentOrders[].carrier` | string | no |  |
| `shipmentOrders[].shipmentMethod` | string | no |  |
| `shipmentOrders[].packingNotes` | string | no |  |
| `shipmentOrders[].details[]` | array<object> | no |  |
| `shipmentOrders[].thirdPartyAccount` | object | no |  |
| `shipmentOrders[].channelOrderCode` | string | no |  |
| `shipmentOrders[].storeName` | string | no |  |
| `shipmentOrders[].woPriority` | string | no |  |
| `shipmentOrders[].plannedPickupDate` | string | no |  |
| `shipmentOrders[].plannedDeliveryDate` | string | no |  |
| `shipmentOrders[].trackingNumber` | string | no |  |
| `shipmentOrders[].masterEDIReferences` | string | no |  |
| `shipmentOrders[].invoiceCustomer` | string | no |  |
| `shipmentOrders[].invoiceAddress` | string | no |  |
| `shipmentOrders[].invoiceAddressText` | string | no |  |
| `shipmentOrders[].invoiceAddressDirections` | string | no |  |
| `shipmentOrders[].invoiceState` | string | no |  |
| `shipmentOrders[].invoiceCountry` | string | no |  |
| `shipmentOrders[].invoiceCity` | string | no |  |
| `shipmentOrders[].invoicePostalCode` | string | no |  |
| `shipmentOrders[]` | array<object> | no |  |
| `shipmentOrders[].thirdPartyAccount.accountNumber` | string | no |  |
| `shipmentOrders[].thirdPartyAccount.address` | object | no |  |
| `shipmentOrders[].thirdPartyAccount.address.addressDirections` | string | no |  |
| `shipmentOrders[].thirdPartyAccount.address.adressText` | string | no |  |
| `shipmentOrders[].thirdPartyAccount.address.city` | string | no |  |
| `shipmentOrders[].thirdPartyAccount.address.country` | string | no |  |
| `shipmentOrders[].thirdPartyAccount.address.customerAddress` | string | no |  |
| `shipmentOrders[].thirdPartyAccount.address.postalCode` | number | no |  |
| `shipmentOrders[].thirdPartyAccount.address.state` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/:methodName` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-shipment-order.md) for the provider-specific parameters and requirements.

