# Remove Group From Favorites with Instructure

Removes a group from favorites in Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/self/favorites/groups/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Remove Group From Favorites](https://developerdocs.instructure.com/services/canvas/resources/favorites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Canvas group ID. |
