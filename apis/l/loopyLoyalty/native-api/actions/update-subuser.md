# Update Subuser with Loopy Loyalty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subuser/:id`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Update Subuser](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_updateSubuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Subuser ID. |
| `label` | body | `string` | no | Label for the sub-user for easy recognition. |
| `username` | body | `string` | no | Subuser username. |
| `password` | body | `string` | no | Subuser password. |
| `status` | body | `string` | no | Subuser status. |
| `location.id` | body | `string` | no | Subuser location ID. |
