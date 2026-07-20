# Update Item Allocation with Aspire

## Endpoint

- **Method:** `PUT`
- **Path:** `ItemAllocations`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Item Allocation](https://guide.youraspire.com/apidocs/itemallocations-12)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ItemAllocationId` | body | `list<number>` | yes |
| `InventoryLocationID` | body | `list<number>` | yes |
| `CatalogItemID` | body | `list<number>` | yes |
| `WorkTicketID` | body | `list<number>` | yes |
| `Quantity` | body | `string` | yes |
| `AllocationDate` | body | `string` | yes |
