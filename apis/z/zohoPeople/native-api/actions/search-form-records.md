# Search Form Records with Zoho People

Finds records in a Zoho People form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/forms/:formLinkName/getRecords`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Search Form Records](https://www.zoho.com/people/api/forms-api/search-record.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
| `searchParams` | query | `string` | yes | Zoho searchParams expression, for example {searchField:'Employeestatus',searchOperator:'Is',searchText:'Active'}. |
| `slIndex` | query | `number` | no | Record index to start fetching from. Zoho record indexes start at 1. |
| `limit` | query | `number` | no | Maximum number of records to fetch. Zoho documents a maximum of 200. |
