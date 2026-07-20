# List Contacts with MindMe

Retrieves contacts from MindMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Contact/GetContactByFilter`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [List Contacts](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Contact~1GetContactByFilter/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | query | `string` | no |
| `BirthdayFiltersBySubCategory` | query | `string` | no |
| `contactId` | query | `string` | no |
| `DateField` | query | `string` | no |
| `DateFieldFilterIntervalType` | query | `string` | no |
| `DateFieldIntervalRangeType` | query | `string` | no |
| `DateIntervalLength` | query | `string` | no |
| `EndDate` | query | `string` | no |
| `filterBy` | query | `string` | no |
| `IsFilterAfterStartDate` | query | `string` | no |
| `IsFilterByBirthDate` | query | `string` | no |
| `IsFilterByContactUpdateDate` | query | `string` | no |
| `IsFilterByMonth` | query | `string` | no |
| `listType` | query | `string` | no |
| `Month` | query | `string` | no |
| `pageNumber` | query | `string` | no |
| `pageSize` | query | `string` | no |
| `searchValue` | query | `string` | no |
| `sortColumnName` | query | `string` | no |
| `sortingDirection` | query | `string` | no |
| `sortPreferencePage` | query | `string` | no |
| `StartDate` | query | `string` | no |
| `typeId` | query | `string` | no |
| `userId` | query | `string` | no |
