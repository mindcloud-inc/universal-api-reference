# Search Projects with ArcSite

Finds projects in ArcSite using search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/search`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Search Projects](https://dev.arcsite.com/#search-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_name` | body | `string` | no | Filter projects whose name contains this value. |
| `tags[]` | body | `array<string>` | no | Filter projects by tags. |
