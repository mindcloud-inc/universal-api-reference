# Create Form Record with Zoho People

Creates a record in a Zoho People form.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/forms/json/:formLinkName/insertRecord`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Create Form Record](https://www.zoho.com/people/api/insert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
| `inputData` | body | `string` | yes | Zoho form field payload, for example {Single_Line_1:"a1",Lookup_1:"705358000000229001"}. |
| `isDraft` | body | `boolean` | no | Set to true to save the record as a draft. |
