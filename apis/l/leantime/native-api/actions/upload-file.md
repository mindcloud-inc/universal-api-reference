# Upload File with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Upload File](https://docs.leantime.io/api/classes/Leantime/Domain/Files/Services/Files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `object` | yes | Leantime file payload. |
| `module` | body | `string` | yes | The Leantime module name. |
| `entityId` | body | `number` | yes | The target entity id. |
| `entity` | body | `object` | no | Optional entity context. |
