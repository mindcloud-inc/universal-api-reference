# Create Subuser with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/subuser`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Create Subuser](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createSubuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Label for the sub-user for easy recognition. |
| `username` | body | `string` | yes | Subuser username. |
| `password` | body | `string` | yes | Subuser password. |
| `status` | body | `string` | no | Subuser status. |
| `location.id` | body | `string` | no | Subuser location ID. |
