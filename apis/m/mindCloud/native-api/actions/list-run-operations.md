# List Run Operations with MindCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/runs/:runId/operations`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [List Run Operations](https://connect.mindcloud.co/v2/openapi.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated fields to return. Leave empty to return all fields. The API always includes id. |
| `runId` | path | `string` | yes | Run ID for this MindCloud v2 request. |
| `where` | query | `string` | no | Optional Where query parameter documented by the MindCloud v2 API. |
