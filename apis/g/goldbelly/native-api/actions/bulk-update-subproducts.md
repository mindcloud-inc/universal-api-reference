# Bulk Update Subproducts with Goldbelly

## Endpoint

- **Method:** `POST`
- **Path:** `subproducts/bulk_update`
- **Base URL:** `https://api.goldbelly.com/v1/`
- **Official documentation:** [Bulk Update Subproducts](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#subproducts_bulk_update_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subproducts[]` | body | `array<object>` | yes | Subproducts to update. Each item must include SKU and may include inventory. |
| `subproducts[].sku` | body | `string` | yes | Subproduct SKU. |
| `subproducts[].inventory` | body | `number` | no | Subproduct inventory quantity. |
