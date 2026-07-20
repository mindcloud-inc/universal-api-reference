# Update Action Item with IceCubes

## Endpoint

- **Method:** `PATCH`
- **Path:** `/action-items/:id`
- **Base URL:** `https://icecubes.app/api/public`
- **Official documentation:** [Update Action Item](https://icecubes.app/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The action item ID to update. |
| `completed` | body | `boolean` | no | Mark the action item complete or incomplete. |
| `text` | body | `string` | no | Updated action item text. |
