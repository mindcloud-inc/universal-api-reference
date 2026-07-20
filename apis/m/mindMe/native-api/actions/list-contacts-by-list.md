# List Contacts By List with MindMe

Retrieves contacts from a list in MindMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/List/GetContactsByList`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [List Contacts By List](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1List~1GetContactsByList/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | query | `string` | no |
| `BirthdayFiltersBySubCategory` | query | `string` | no |
| `categoryFilterBy` | query | `string` | no |
| `DateField` | query | `string` | no |
| `DateFieldFilterIntervalType` | query | `string` | no |
| `DateFieldIntervalRangeType` | query | `string` | no |
| `DateIntervalLength` | query | `string` | no |
| `EndDate` | query | `string` | no |
| `listId` | query | `string` | no |
| `listType` | query | `string` | no |
| `pageNumber` | query | `string` | no |
| `pageSize` | query | `string` | no |
| `searchValue` | query | `string` | no |
| `sortColumnName` | query | `string` | no |
| `sortingDirection` | query | `string` | no |
| `StartDate` | query | `string` | no |
| `typeId` | query | `string` | no |
