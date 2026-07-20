# Insert Shipment Order with Logiwa Legacy WMS

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/:methodName`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [Insert Shipment Order](https://developer.logiwa.com/?id=5df0db19e6466c2eec992f4d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentOrders[].Code` | body | `string` | no | — |
| `shipmentOrders[].Details[].InventoryItem` | body | `string` | no | — |
| `methodName` | path | `list<string>` | yes | ***InsertShipmentOrder Endpoint***: - Lists the orders as a group and if one of the orders fails to import, the whole request operations will be rolled back and none of the orders will be imported  ***InsertShipmentOrderWithBulkResult***: - Evaluates orders separately. The successful records will be created and the failed records will be listed with an error message in the response. |
| `shipmentOrders[].Depositor` | body | `string` | no | — |
| `shipmentOrders[].Details[].InventoryItemPackType` | body | `string` | no | — |
| `shipmentOrders[].Details[].PlannedPackQuantity` | body | `string` | no | Planned quantity per defined pack type |
| `shipmentOrders[].WarehouseOrderStatus` | body | `string` | no | — |
| `shipmentOrders[].Details[].notes` | body | `string` | no | — |
| `shipmentOrders[].InventorySite` | body | `string` | no | — |
| `shipmentOrders[].Details[].location` | body | `string` | no | — |
| `shipmentOrders[].Warehouse` | body | `string` | no | — |
| `shipmentOrders[].Details[].lotBatchNo` | body | `string` | no | — |
| `shipmentOrders[].WarehouseOrderType` | body | `string` | no | — |
| `shipmentOrders[].Customer` | body | `string` | no | — |
| `shipmentOrders[].Details[].giftNote` | body | `string` | no | — |
| `shipmentOrders[].CustomerAddress` | body | `string` | no | — |
| `shipmentOrders[].Details[].freeAttr1` | body | `string` | no | — |
| `shipmentOrders[].Details[].freeAttr2` | body | `string` | no | — |
| `shipmentOrders[].OrderDate` | body | `string` | no | — |
| `shipmentOrders[].Details[].freeAttr3` | body | `string` | no | — |
| `shipmentOrders[].State` | body | `string` | no | — |
| `shipmentOrders[].Country` | body | `string` | no | — |
| `shipmentOrders[].Details[].notes1` | body | `string` | no | — |
| `shipmentOrders[].City` | body | `string` | no | — |
| `shipmentOrders[].Details[].notes2` | body | `string` | no | — |
| `shipmentOrders[].Details[].notes3` | body | `string` | no | — |
| `shipmentOrders[].PostalCode` | body | `string` | no | — |
| `shipmentOrders[].Details[].channelorderdetailcode` | body | `string` | no | — |
| `shipmentOrders[].Phone` | body | `string` | no | — |
| `shipmentOrders[].Details[].detailEDIReferences` | body | `string` | no | — |
| `shipmentOrders[].Email` | body | `string` | no | — |
| `shipmentOrders[].AdressText` | body | `string` | no | — |
| `shipmentOrders[].Details[].salesUnitPrice` | body | `string` | no | — |
| `shipmentOrders[].PartyAdressType` | body | `string` | no | — |
| `shipmentOrders[].EDIBillTo` | body | `string` | no | — |
| `shipmentOrders[].BusinessDaysInTransit` | body | `number` | no | — |
| `shipmentOrders[].IsCheckAllocationAvailability` | body | `boolean` | no | — |
| `shipmentOrders[].Carrier` | body | `string` | no | — |
| `shipmentOrders[].Prefix` | body | `string` | no | — |
| `shipmentOrders[].Driver` | body | `string` | no | — |
| `shipmentOrders[].plannedShipDate` | body | `string` | no | — |
| `shipmentOrders[].earliestShipDate` | body | `string` | no | — |
| `shipmentOrders[].latestShipDate` | body | `string` | no | — |
| `shipmentOrders[].earliestDeliveryDate` | body | `string` | no | — |
| `shipmentOrders[].latestDeliveryDate` | body | `string` | no | — |
| `shipmentOrders[].warehouseReceipt` | body | `string` | no | — |
| `shipmentOrders[].notes` | body | `string` | no | — |
| `shipmentOrders[].customeRefCode` | body | `string` | no | — |
| `shipmentOrders[].depositorRefCode` | body | `string` | no | — |
| `shipmentOrders[].customerOrderNo` | body | `string` | no | — |
| `shipmentOrders[].giftNote` | body | `string` | no | — |
| `shipmentOrders[].deliveryNoteNo` | body | `string` | no | — |
| `shipmentOrders[].extraNotes` | body | `string` | no | — |
| `shipmentOrders[].instructions` | body | `string` | no | — |
| `shipmentOrders[].extraNotes1` | body | `string` | no | — |
| `shipmentOrders[].extraNotes1` | body | `string` | no | — |
| `shipmentOrders[].extraNotes3` | body | `string` | no | — |
| `shipmentOrders[].extraNotes4` | body | `string` | no | — |
| `shipmentOrders[].extraNotes5` | body | `string` | no | — |
| `shipmentOrders[].channel` | body | `string` | no | — |
| `shipmentOrders[].carrier` | body | `string` | no | — |
| `shipmentOrders[].shipmentMethod` | body | `string` | no | — |
| `shipmentOrders[].packingNotes` | body | `string` | no | — |
| `shipmentOrders[].Details[]` | body | `array<object>` | no | — |
| `shipmentOrders[].ThirdPartyAccount` | body | `object` | no | — |
| `shipmentOrders[].channelOrderCode` | body | `string` | no | — |
| `shipmentOrders[].storeName` | body | `string` | no | — |
| `shipmentOrders[].woPriority` | body | `string` | no | — |
| `shipmentOrders[].plannedPickupDate` | body | `string` | no | — |
| `shipmentOrders[].plannedDeliveryDate` | body | `string` | no | — |
| `shipmentOrders[].trackingNumber` | body | `string` | no | — |
| `shipmentOrders[].masterEDIReferences` | body | `string` | no | — |
| `shipmentOrders[].invoiceCustomer` | body | `string` | no | — |
| `shipmentOrders[].invoiceAddress` | body | `string` | no | — |
| `shipmentOrders[].invoiceAddressText` | body | `string` | no | — |
| `shipmentOrders[].invoiceAddressDirections` | body | `string` | no | — |
| `shipmentOrders[].invoiceState` | body | `string` | no | — |
| `shipmentOrders[].invoiceCountry` | body | `string` | no | — |
| `shipmentOrders[].invoiceCity` | body | `string` | no | — |
| `shipmentOrders[].invoicePostalCode` | body | `string` | no | — |
| `shipmentOrders[]` | body | `array<object>` | no | — |
| `shipmentOrders[].ThirdPartyAccount.AccountNumber` | body | `string` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address` | body | `object` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address.AddressDirections` | body | `string` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address.AdressText` | body | `string` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address.City` | body | `string` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address.Country` | body | `string` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address.CustomerAddress` | body | `string` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address.PostalCode` | body | `number` | no | — |
| `shipmentOrders[].ThirdPartyAccount.Address.State` | body | `string` | no | — |
