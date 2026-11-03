# Delete Product Quantity with Rithum for Brands

Remove all Quantity for a Product at a specified Distribution Center.

## Endpoint

- **Method:** `DELETE`
- **Path:** `Products(:id)/DCQuantities(:distributionCenterID)`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Delete Product Quantity](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=21dcd3491bd5d1d42d9eea40604bcbdf#concept-8661__section-DistributionCenterQuantities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `distributionCenterID` | path | `number` | yes |
