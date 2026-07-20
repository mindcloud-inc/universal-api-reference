# Add Photo to Project with CompanyCam

Adds a photo to a CompanyCam project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/photos`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Add Photo to Project](https://docs.companycam.com/reference/createprojectphoto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `photo.coordinates.lat` | body | `number` | no | — |
| `photo.uri` | body | `string` | yes | — |
| `photo.captured_at` | body | `date` | yes | Timestamp when the photo was captured at. |
| `photo.coordinates.lon` | body | `number` | no | — |
| `project_id` | path | `string` | yes | — |
| `photo` | body | `object` | no | — |
| `photo.description` | body | `string` | no | A description of the Photo. |
| `photo.coordinates` | body | `object` | no | — |
| `photo.tags` | body | `list<string>` | no | Send multiple values as a array. |
