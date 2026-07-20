# Get Showcase with Vimeo

Retrieves a showcase record from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/albums/:album_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Get Showcase](https://developer.vimeo.com/api/reference/showcases#get_showcase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `album_id` | path | `number` | yes | The ID of the showcase. |
