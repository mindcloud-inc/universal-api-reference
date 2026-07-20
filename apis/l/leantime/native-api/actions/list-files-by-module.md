# List Files By Module with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [List Files By Module](https://docs.leantime.io/api/classes/Leantime/Domain/Files/Services/Files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.module` | body | `string` | yes | The Leantime module name. |
| `entityId` | body | `number` | yes | The target entity id. |
| `userId` | body | `number` | no | Optional user id filter. |
