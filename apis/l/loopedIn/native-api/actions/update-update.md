# Update Update with LoopedIn

Updates an existing update in LoopedIn.

## Endpoint

- **Method:** `PUT`
- **Path:** `/updates/:id`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Update Update](https://docs.loopedin.io/#update-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LoopedIn update ID. |
| `title` | body | `string` | no | The updated update title. |
