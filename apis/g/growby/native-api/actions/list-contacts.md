# List Contacts with Growby

Retrieves contacts from Growby.

## Endpoint

- **Method:** `GET`
- **Path:** `/devapi/contacts`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [List Contacts](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNumber` | query | `number` | no | Page number to fetch. Growby documents values from 1 to 20. |
| `pageSize` | query | `number` | no | Number of contacts to return per page. Growby documents values from 1 to 20. |
| `sortColumn` | query | `string` | no | Column name used for sorting. Supported values are Id, AccountId, FirstName, LastName, Email, MobileNumber, City, and State. |
| `sortOrder` | query | `string` | no | Sort direction. Supported values are ASC or DESC. |
