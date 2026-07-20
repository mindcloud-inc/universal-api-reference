# Create Item Allocation with Aspire

Creates a new pay code in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `ItemAllocations`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Item Allocation](https://guide.youraspire.com/apidocs/itemallocations-3)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AllocationDate` | body | `string` | yes |
| `CatalogItemID` | body | `list<number>` | yes |
| `InventoryLocationID` | body | `list<number>` | yes |
| `WorkTicketID` | body | `list<number>` | yes |
| `Quantity` | body | `string` | yes |
