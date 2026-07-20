# List Notebook Versions with Teamwork Projects

Retrieves notebook versions from Teamwork Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/notebooks/{{notebookId}}/versions.json`
- **Base URL:** `{apiEndPoint}projects/api/v3`
- **Official documentation:** [List Notebook Versions](https://apidocs.teamwork.com/docs/teamwork/v3/notebooks/get-projects-api-v3-notebooks-notebook-id-versions-json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notebookId` | path | `number` | yes | Teamwork notebook ID. |
