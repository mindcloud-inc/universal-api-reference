# Get Product Pricing with Megaventory

Retrieves pricing for a product from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductPriceGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Get Product Pricing](https://api.megaventory.com/v2017a/json/metadata?op=ProductPriceGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | body | `number` | no | Megaventory product ID to price. |
| `DocumentTypeId` | body | `number` | no | Document type that affects the calculated price. |
| `Quantity` | body | `number` | no | Quantity used for the price lookup. |
| `SupplierClientId` | body | `number` | no | Supplier or client context for the price lookup. |
| `Currency` | body | `string` | no | Currency code for the requested price. |
| `IssueDate` | body | `date` | no | Date Megaventory should use when resolving the price. |
