# Add Course To Favorites with Instructure

Adds a course to favorites in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/self/favorites/courses/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Add Course To Favorites](https://developerdocs.instructure.com/services/canvas/resources/favorites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Canvas course ID. |
