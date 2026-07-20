# Create Inventory Item with Absinthe

Creates a reward item in an Absinthe campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Create Inventory Item](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `xp_cost` | body | `number` | yes |
| `total_units` | body | `number` | yes |
