# Update Task with Twenty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/tasks/:id`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Update Task](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `bodyV2` | body | `string` | no |
| `status` | body | `string` | no |
| `title` | body | `string` | no |
| `dueAt` | body | `date` | no |
