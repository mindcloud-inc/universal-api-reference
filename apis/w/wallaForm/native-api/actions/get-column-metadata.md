# Get Column Metadata with Walla Form

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspaceKey/project/:projectKey/response/list/:columnKey`
- **Base URL:** `https://walla-api.data-lab.workers.dev`
- **Official documentation:** [Get Column Metadata](https://walla-api.data-lab.workers.dev/ui)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceKey` | path | `string` | yes | The Walla workspace key. |
| `projectKey` | path | `string` | yes | The Walla project key. |
| `columnKey` | path | `string` | yes | The column key for a project field. |
