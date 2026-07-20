# Create Project with Dremio

Creates a new project in Dremio.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create Project](https://docs.dremio.com/dremio-cloud/api/projects/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cloudId` | body | `string` | yes |
| `name` | body | `string` | yes |
