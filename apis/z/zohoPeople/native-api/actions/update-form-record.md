# Update Form Record with Zoho People

Updates a record in a Zoho People form.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/forms/json/:formLinkName/updateRecord`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Update Form Record](https://www.zoho.com/people/api/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
| `recordId` | body | `string` | yes | Record ID of the Zoho People record to update. |
| `inputData` | body | `string` | yes | Zoho form field payload containing the fields to update. |
| `isDraft` | body | `boolean` | no | Set to true to save the updated record as a draft. |
| `tabularData` | body | `string` | no | Optional tabular section payload for rows that should be added, updated, or deleted. |
