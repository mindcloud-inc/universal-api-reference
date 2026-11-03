# Update Product Quantity with Rithum for Brands

Update Product Quantity at one or more Distribution Centers.

## Endpoint

- **Method:** `POST`
- **Path:** `Products(:productID)/UpdateQuantity`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Update Product Quantity](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=c0ec1b491bd5d1d42d9eea40604bcb8d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productID` | path | `string` | yes | The Rithum-defined unique ID (not the Sku value) of the product you want to update quantities for. |
| `Updates[].DistributionCenterID` | body | `number` | no | Rithum's Distribution Center Unique ID. |
| `Updates[].Quantity` | body | `number` | no | Available Quantity for the product at the Distribution Center ID provided. |
| `UpdateType` | body | `list<string>` | yes | This value determines how the platform will interpret the quantity. |
| `Updates` | body | `array` | no | A list of Qtys for this product at each Distribution Center.  *Note: 'Quantity' and 'Distribution Center ID' are required arguments* |
