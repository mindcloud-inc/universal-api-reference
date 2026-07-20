# Update item or collection with Nuclino

Updates an existing item or collection in Nuclino.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:id`
- **Base URL:** `https://api.nuclino.com/v0`
- **Official documentation:** [Update item or collection](https://help.nuclino.com/fa38d15f-items-and-collections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `string` | no |
| `id` | path | `string` | yes |
| `title` | body | `string` | no |
