# Duplicate Project with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Duplicate Project](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.projectId` | body | `number` | yes | The project to duplicate. |
| `params.clientId` | body | `number` | yes | The client ID for the duplicated project. |
| `params.projectName` | body | `string` | yes | The new project name. |
| `params.userStartDate` | body | `string` | no | The duplicated project start date in the workspace user format. |
| `params.assignSameUsers` | body | `boolean` | no | Whether to copy the source project's user assignments. |
