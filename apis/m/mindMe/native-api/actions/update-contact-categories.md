# Update Contact Categories with MindMe

Adds or removes contact categories in MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contact/AddOrRemoveContactsByCategories`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [Update Contact Categories](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1AddOrRemoveContactsByCategories/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `categoryIds` | body | `string` | no |
| `contactCategory` | body | `string` | no |
| `contactIds` | body | `string` | no |
| `searchValue` | body | `string` | no |
