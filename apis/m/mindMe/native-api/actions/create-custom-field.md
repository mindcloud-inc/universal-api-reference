# Create Custom Field with MindMe

Creates a new custom field in MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/CustomFields/SaveCustomField`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [Create Custom Field](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CustomFields~1SaveCustomField/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | no |
| `accountIds` | body | `string` | no |
| `description` | body | `string` | no |
| `fieldName` | body | `string` | no |
| `fieldType` | body | `string` | no |
| `group` | body | `string` | no |
| `groupId` | body | `string` | no |
| `internalFieldName` | body | `string` | no |
| `isReadOnly` | body | `string` | no |
| `options` | body | `string` | no |
| `parentAccountId` | body | `string` | no |
| `userId` | body | `string` | no |
