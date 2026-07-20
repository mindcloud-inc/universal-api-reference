# Get Form Record with Zoho People

Retrieves a record from a Zoho People form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/forms/:formLinkName/getDataByID`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Form Record](https://www.zoho.com/people/api/forms-api/fetch-single.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
| `recordId` | query | `string` | yes | Record ID from Zoho People, typically obtained from a bulk-records or search response. |
