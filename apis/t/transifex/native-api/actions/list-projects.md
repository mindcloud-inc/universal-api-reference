# List Projects with Transifex

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://rest.api.transifex.com`
- **Official documentation:** [List Projects](https://developers.transifex.com/reference/get_projects.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[organization]` | query | `string` | yes | Return projects for this organization id, for example o:mindcloud. |
