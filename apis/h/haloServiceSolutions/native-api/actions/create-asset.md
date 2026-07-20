# Create Asset with Halo Service Solutions

Creates a new asset in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/Asset`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create Asset](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inventory_number` | body | `string` | yes |
| `site_id` | body | `number` | yes |
| `assettype_id` | body | `number` | yes |
