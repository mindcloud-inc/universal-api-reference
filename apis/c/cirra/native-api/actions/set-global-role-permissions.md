# Set Global Role Permissions with Cirra

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/cirra/roles/:roleId/permissions/global`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleId` | path | `list` | yes | — |
| `allowRead` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
| `allowCreate` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
| `allowUpdate` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
| `allowDelete` | body | `boolean` | no | Optional CRUD override flag. Omit unchanged operations. |
