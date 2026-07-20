# Update Workflow Task Notes with Documentum

## Endpoint

- **Method:** `PUT`
- **Path:** `/repositories/{repositoryName}/processes/{processName}/{processId}/{taskName}/{taskId}/notes`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Update Workflow Task Notes](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `processName` | path | `string` | yes | Name of the dm_workflow process. |
| `processId` | path | `string` | yes | r_object_id of the dm_workflow process. |
| `taskName` | path | `string` | yes | Name of the workflow activity. |
| `taskId` | path | `string` | yes | r_object_id of the dmi_queue_item task. |
| `properties` | body | `object` | yes | JSON note payload, for example task_note. |
