# Update Client with Harvest

Updates an existing client in Harvest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/clients/:id`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Update Client](https://help.getharvest.com/api-v2/clients-api/clients/clients/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | no |
| `is_active` | body | `boolean` | no |
| `address` | body | `string` | no |
| `currency` | body | `string` | no |
