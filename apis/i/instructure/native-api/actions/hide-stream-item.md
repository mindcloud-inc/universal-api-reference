# Hide Stream Item with Instructure

Hides a stream item in Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/self/activity_stream/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Hide Stream Item](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.ignore_stream_item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the activity stream item to hide. |
