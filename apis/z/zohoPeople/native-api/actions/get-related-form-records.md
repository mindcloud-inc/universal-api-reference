# Get Related Form Records with Zoho People

Retrieves related records from a Zoho People form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/forms/:formLinkName/getRelatedRecords`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Related Form Records](https://www.zoho.com/people/api/forms-api/get-single.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
| `parentModule` | query | `string` | yes | Parent module whose related records should be fetched, such as employee. |
| `id` | query | `string` | yes | Parent record ID used to fetch related records. |
| `lookupfieldName` | query | `string` | no | Optional lookup field name to restrict which related records are returned. |
| `slIndex` | query | `number` | no | Record index to start fetching from. Zoho record indexes start at 1. |
| `limit` | query | `number` | no | Maximum number of related records to fetch. Zoho documents a maximum of 200. |
