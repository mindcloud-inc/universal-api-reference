# Submit Inventory Update with Amazon Vendor

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/directFulfillment/inventory/v1/warehouses/:warehouseId/items`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Submit Inventory Update](https://developer-docs.amazon.com/sp-api/reference/submitinventoryupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `warehouseId` | path | `string` | yes | Identifier for the warehouse for which to update inventory. |
| `inventory` | body | `object` | no | Inventory details required to update some or all items for the requested warehouse. |
| `sellingParty` | body | `object` | yes | ID of the selling party or vendor. |
| `partyId` | body | `string` | yes | Assigned identification for the party. |
| `isFullUpdate` | body | `boolean` | yes | When true, this request contains a full feed; otherwise it contains a partial feed. A full feed must include all warehouse items, and omitted items become unavailable. A partial feed should include only items whose inventory must change; other items remain unchanged. |
| `items[]` | body | `array<object>` | yes | A list of inventory items with updated details, including quantity available. Send multiple values as a array. |
| `buyerProductIdentifier` | body | `string` | no | The buyer-selected product identifier for the item. Submit either this value or the vendor product identifier. |
| `vendorProductIdentifier` | body | `string` | no | The vendor-selected product identifier for the item. Submit either this value or the buyer product identifier. |
| `availableQuantity` | body | `object` | yes | Total item quantity available in the warehouse. |
| `amount` | body | `number` | no | Quantity of units available for a specific item. |
| `unitOfMeasure` | body | `string` | yes | Unit of measure for the available quantity. |
| `isObsolete` | body | `boolean` | no | When true, the item is permanently unavailable. |
