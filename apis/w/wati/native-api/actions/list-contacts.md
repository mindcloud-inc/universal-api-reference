# List Contacts with Wati

Retrieves contacts from Wati using optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/getContacts`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [List Contacts](https://docs.wati.io/reference/get_api-v1-getcontacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | no | Number of contacts to return per page. |
| `pageNumber` | query | `number` | no | Page number to return. |
| `name` | query | `string` | no | Filter contacts by name. |
| `attribute` | query | `string` | no | Filter contacts by attribute. |
| `createdDate` | query | `date` | no | Filter contacts by created date. |
