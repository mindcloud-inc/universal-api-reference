# Create Issue with MantisBT

Creates a new issue in MantisBT.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Create Issue](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category.name` | body | `string` | yes | Existing category name for the issue, such as General |
| `description` | body | `string` | yes | Issue description |
| `project.id` | body | `number` | yes | Project ID where the issue will be created |
| `summary` | body | `string` | yes | Issue summary |
