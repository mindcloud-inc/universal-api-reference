# Set Role App Permissions with Cirra

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/cirra/roles/:roleId/permissions/apps/:appId`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleId` | path | `list` | yes | — |
| `appId` | path | `list` | yes | — |
| `allowRead` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
| `allowCreate` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
| `allowUpdate` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
| `allowDelete` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
