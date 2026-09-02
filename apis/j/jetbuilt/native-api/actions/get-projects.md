# Get Projects with Jetbuilt

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:id`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Get Projects](https://api.jetbuilt.com/customers#projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Project ID |
| `query` | query | `string` | no | — |
| `active` | query | `boolean` | no | (true/false) returns projects in an active stage when true; otherwise returns projects in non-active stages |
| `stage` | query | `string` | no | Filter projects by stage (a single stage name or a comma separated list - param is ignored when active param is present) Send multiple values as a array. |
| `min_created_at` | query | `string` | no | — |
| `min_updated_at` | query | `string` | no | — |
