# List Version Insights with Openlayer

Retrieves insights for a version in Openlayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/versions/:versionId/insights`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [List Version Insights](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `versionId` | path | `string` | yes | The project version ID. |
| `workspaceId` | query | `string` | yes | Workspace scope for insights. |
