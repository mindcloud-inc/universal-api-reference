# Update Project by External ID with Timelink

Updates an existing project in Timelink by external ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/ext/:extId`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Update Project by External ID](https://api.timelink.io/documentation#/Projects/patch_api_v1_projects_ext__ext-id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extId` | path | `string` | yes | The external reference ID for the project. |
| `name` | body | `string` | no | Updated project name. |
| `client_id` | body | `string` | no | The Timelink client ID for this project. |
