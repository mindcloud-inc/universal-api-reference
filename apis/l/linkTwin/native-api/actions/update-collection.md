# Update Collection with LinkTwin

Updates an existing collection in LinkTwin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/collection/:id/update`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Update Collection](https://linktw.in/developers#update-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Collection ID. |
| `name` | body | `string` | no | Collection name. |
| `slug` | body | `string` | no | Rotator slug. |
| `description` | body | `string` | no | Collection description. |
| `color` | body | `string` | no | Collection badge color in HEX. |
| `public` | body | `boolean` | no | Whether the collection is public. |
| `starred` | body | `boolean` | no | Whether the collection is starred. |
