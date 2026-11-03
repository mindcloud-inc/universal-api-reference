# List Product Quantities with Rithum for Brands

Retrieve Quantities for a specified Product at all Distribution Centers.

## Endpoint

- **Method:** `GET`
- **Path:** `Products(:prodID)/DCQuantities`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [List Product Quantities](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=18ecd7491bd5d1d42d9eea40604bcb55)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductID` | path | `string` | no | The Rithum-defined unique ID (not the Sku value) of the product.  *Bugged* |
| `prodID` | path | `string` | yes | — |
