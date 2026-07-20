# Add Label to Project with CompanyCam

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:projectId/labels`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Add Label to Project](https://docs.companycam.com/reference/listprojects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project.labels` | body | `string` | no | Send multiple values as a array. |
| `projectId` | path | `string` | yes | — |
| `project` | body | `object` | no | — |
