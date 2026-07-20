# Search Records with Bigin by Zoho CRM

Finds records in Bigin by Zoho CRM by criteria, email, phone, or word.

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName/search`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Search Records](https://www.bigin.com/developer/docs/apis/v2/search-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `list<string>` | yes | The API name of the module to search. |
| `criteria` | query | `string` | no | Field-expression criteria such as (Last_Name:equals:Burns). |
| `email` | query | `string` | no | Search records by email address. |
| `phone` | query | `string` | no | Search records by phone number. |
| `word` | query | `string` | no | Search records by a word value. |
