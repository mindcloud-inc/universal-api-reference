# Update Label with EZICHEQ

Updates a label in EZICHEQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/label/v1/:labelNumber`
- **Base URL:** `https://api.ezicheq.com`
- **Official documentation:** [Update Label](https://developer.ezicheq.com/docs/endpoints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `asset_description` | body | `string` | no |
| `item_type_id` | body | `string` | no |
| `label_number` | path | `string` | yes |
| `serial_number` | body | `string` | no |
| `status` | body | `string` | no |
| `item_type_id` | body | `string` | no |
| `serial_number` | body | `string` | no |
| `asset_description` | body | `string` | no |
| `status` | body | `string` | no |
