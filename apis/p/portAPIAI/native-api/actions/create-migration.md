# Create Migration with Port API AI

Creates a migration in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/migrations`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Migration](https://docs.port.io/api-reference/create-a-migration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sourceBlueprint` | body | `string` | yes |
| `mapping` | body | `object` | yes |
