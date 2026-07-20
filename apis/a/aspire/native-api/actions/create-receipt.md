# Create Receipt with Aspire

Creates a new receipt in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `Receipts`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Receipt](https://guide.youraspire.com/apidocs/receipts-9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ReceiptItems[].itemAllocations[].workTicketID` | body | `list<number>` | no | Item allocations require either a WorkTicketID or an InventoryLocationID, can't have both. |
| `ReceiptItems[].receiptItemID` | body | `number` | yes | — |
| `VendorID` | body | `list<string>` | yes | — |
| `ReceiptItems[].catalogItemID` | body | `list<number>` | no | — |
| `ReceiptItems[].itemAllocations[].inventoryLocationID` | body | `list<number>` | yes | Item allocations require either a WorkTicketID or an InventoryLocationID, can't have both. |
| `WorkTicketID` | body | `list<number>` | no | — |
| `ReceiptItems[].catalogItemCategoryID` | body | `list<number>` | no | — |
| `ReceiptNote` | body | `string` | no | — |
| `ReceiptItems[].itemAllocations[].itemQuantity` | body | `number` | yes | — |
| `ReceiptItems[].ItemName` | body | `string` | yes | — |
| `VendorInvoiceNum` | body | `string` | no | — |
| `ReceiptItems[].ItemQuantity` | body | `number` | yes | — |
| `VendorInvoiceDate` | body | `string` | no | — |
| `BranchID` | body | `list` | no | — |
| `ReceiptItems[].ItemUnitCost` | body | `number` | yes | — |
| `ReceiptItems[]` | body | `array<object>` | no | There has to be at least one receipt item |
| `ReceiptItems[].ItemType` | body | `list<string>` | yes | — |
| `inventoryLocationID` | body | `list<number>` | no | The ID of an inventory location. Required if no WorkTicketID is provided, to avoid the error: `At least one of WorkTicketID or InventoryLocationID is required.` |
| `ReceiptItems[].ItemEstUnitCost` | body | `number` | no | — |
| `ReceiptItems[].receiptItemPrice` | body | `number` | no | — |
| `ReceivedDate` | body | `string` | no | — |
| `ReceiptItems[].itemAllocations[]` | body | `array<object>` | no | — |
