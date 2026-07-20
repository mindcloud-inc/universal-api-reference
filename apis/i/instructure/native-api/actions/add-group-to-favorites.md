# Add Group To Favorites with Instructure

Adds a group to favorites in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/self/favorites/groups/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Add Group To Favorites](https://developerdocs.instructure.com/services/canvas/resources/favorites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Canvas group ID. |
