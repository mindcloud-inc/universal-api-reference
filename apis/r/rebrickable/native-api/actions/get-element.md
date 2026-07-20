# Get Element with Rebrickable

Retrieves a LEGO element from Rebrickable by element ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/elements/:element_id/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [Get Element](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element_id` | path | `string` | yes | LEGO element ID to look up. |
