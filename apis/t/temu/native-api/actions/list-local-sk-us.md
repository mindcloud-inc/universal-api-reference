# List Local SKUs with Temu

Search the local SKU list

## Endpoint

- **Method:** `POST`
- **Path:** `/router`
- **Base URL:** `https://openapi-b-us.temu.com/openapi`
- **Official documentation:** [List Local SKUs](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=0037738f728b4e81886d17511f2d4f0f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `skuSearchType` | body | `list<string>` | yes | SKU status filter |
| `goodsName` | body | `string` | no | — |
| `goodsSearchTags` | body | `list<number>` | no | Optional.  **Goods search tags:** 1 - Low traffic 4 - Restricted traffic Send multiple values as a array. |
| `catIdList` | body | `string` | no | Category id for search limit of 100 Send multiple values as a array. |
| `skuIdLi` | body | `string` | no | Sku ID for search limit of 200 Send multiple values as a array. |
| `goodsIdList` | body | `string` | no | Product ID for search limit of 100 Send multiple values as a array. |
| `outSkuSnList` | body | `string` | no | OutSkuSn for search limit of 200 Send multiple values as a array. |
| `outGoodsSnLi` | body | `string` | no | OutGoodsSn for search limit of 100 Send multiple values as a array. |
| `goodsCreateTimeFrom` | body | `date` | no | — |
| `goodsCreateTimeTo` | body | `date` | no | — |
| `skuStatusChangeTimeFrom` | body | `date` | no | — |
| `skuStatusChangeTimeTo` | body | `date` | no | — |
| `orderField` | body | `string` | no | — |
| `orderType` | body | `list<number>` | no | — |
