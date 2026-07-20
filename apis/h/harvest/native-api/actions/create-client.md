# Create Client with Harvest

Creates a new client in Harvest.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/clients`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Create Client](https://help.getharvest.com/api-v2/clients-api/clients/clients/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `is_active` | body | `boolean` | no |
| `address` | body | `string` | no |
| `currency` | body | `string` | no |
