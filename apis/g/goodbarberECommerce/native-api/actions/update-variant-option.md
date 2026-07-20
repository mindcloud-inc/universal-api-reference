# Update Variant Option with Goodbarber eCommerce

## Endpoint

- **Method:** `PATCH`
- **Path:** `/publicapi/v2/general/catalog/:webzine_id/option/:option_id/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [Update Variant Option](https://commerce.goodbarber.dev/api/schema_v2/#tag/Catalog-Option/operation/updateOption)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `option_id` | path | `number` | yes | Variant option ID. |
| `name` | body | `string` | no | Updated variant option display name. |
