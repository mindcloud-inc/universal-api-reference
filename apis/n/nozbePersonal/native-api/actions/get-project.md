# Get Project with Nozbe Personal

Retrieves a project from Nozbe Personal by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Get Project](https://api4.nozbe.com/v1/api#/projects/getProjectById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project ID to retrieve. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
