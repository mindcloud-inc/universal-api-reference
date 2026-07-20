# List Folders with Infisical

Retrieves folders from a project environment in Infisical.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/folders`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [List Folders](https://infisical.com/docs/api-reference/endpoints/folders/list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | query | `string` | yes |
| `environment` | query | `string` | yes |
| `path` | query | `string` | yes |
