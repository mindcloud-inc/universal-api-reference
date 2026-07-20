# List Projects with ParseHub

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://www.parsehub.com/api/v2`
- **Official documentation:** [List Projects](https://www.parsehub.com/docs/ref/api/v2/#list-all-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of projects to return. ParseHub accepts values from 1 through 20. |
| `offset` | query | `number` | no | Zero-based offset into the project list. |
| `include_options` | query | `number` | no | Set to 1 to include project options and webhook metadata in each result. |
