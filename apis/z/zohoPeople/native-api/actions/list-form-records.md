# List Form Records with Zoho People

Retrieves records from a Zoho People form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/forms/:formLinkName/getRecords`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [List Form Records](https://www.zoho.com/people/api/bulk-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
| `slIndex` | query | `number` | no | Record index to start fetching from. Zoho record indexes start at 1. |
| `limit` | query | `number` | no | Maximum number of records to fetch in this request. Zoho documents a maximum of 200. |
| `SearchColumn` | query | `string` | no | Optional employee column to search, such as EMPLOYEEID or EMPLOYEEMAILALIAS. |
| `SearchValue` | query | `string` | no | Value to match for the selected search column. |
| `modifiedtime` | query | `number` | no | Fetch only records added or modified after this Unix timestamp in milliseconds. |
