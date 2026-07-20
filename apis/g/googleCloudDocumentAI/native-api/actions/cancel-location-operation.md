# Cancel Location Operation with Google Cloud Document AI

Cancels an operation in a Google Cloud Document AI location.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/operations/:operationsId:cancel`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Cancel Location Operation](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.operations/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operationsId` | path | `string` | no | Long-running operation ID. |
