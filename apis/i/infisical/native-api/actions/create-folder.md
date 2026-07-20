# Create Folder with Infisical

Creates a new folder in an Infisical environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/folders`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Create Folder](https://infisical.com/docs/api-reference/endpoints/folders/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | body | `string` | yes |
| `environment` | body | `string` | yes |
| `name` | body | `string` | yes |
