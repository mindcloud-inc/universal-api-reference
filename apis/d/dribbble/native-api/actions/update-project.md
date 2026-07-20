# Update Project with Dribbble

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.dribbble.com/v2`
- **Official documentation:** [Update Project](https://developer.dribbble.com/v2/projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Dribbble project ID. |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
