# Create Config with ConfigCat

Creates a new config in ConfigCat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/products/:productId/configs`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Create Config](https://configcat.com/docs/api/reference/create-config/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | The identifier of the Product. |
| `config` | body | `object` | yes | Raw ConfigCat config body. Create requires at least name. |
