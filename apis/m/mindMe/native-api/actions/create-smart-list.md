# Create Smart List with MindMe

Creates a new smart list in MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/List/SaveSmartList`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [Create Smart List](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1List~1SaveSmartList/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | no |
| `globalAnyAllOperator` | body | `string` | no |
| `listName` | body | `string` | no |
| `smartListConditions` | body | `string` | no |
| `userId` | body | `string` | no |
