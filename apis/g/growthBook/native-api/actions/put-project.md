# Edit a single project with GrowthBook

Updates an existing project in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Edit a single project](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `name` | body | `string` | no | Project name. |
| `description` | body | `string` | no | Project description. |
| `publicId` | body | `string` | no | URL-safe slug (lowercase letters, numbers, dashes). |
| `settings` | body | `object` | no | Project settings. |
