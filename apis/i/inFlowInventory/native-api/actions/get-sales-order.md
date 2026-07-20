# Get Sales Order with inFlow Inventory

Retrieves an existing sales order from inFlow Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales-orders/:salesOrderId`
- **Base URL:** `https://cloudapi.inflowinventory.com/{companyId}`
- **Official documentation:** [Get Sales Order](https://cloudapi.inflowinventory.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesOrderId` | path | `string` | yes | The inFlow sales order ID. |
