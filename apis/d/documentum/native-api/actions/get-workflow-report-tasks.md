# Get Workflow Report Tasks with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/d2-workflows/{workflowId}/d2-report-tasks`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Get Workflow Report Tasks](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `workflowId` | path | `string` | yes | Workflow ID whose report tasks should be returned. |
| `filterName` | query | `string` | no | Optional D2-Config workflow filter name. |
