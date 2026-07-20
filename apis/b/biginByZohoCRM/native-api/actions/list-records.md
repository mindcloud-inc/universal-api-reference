# List Records with Bigin by Zoho CRM

Retrieves records from a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `GET`
- **Path:** `/:module_api_name`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [List Records](https://www.bigin.com/developer/docs/apis/v2/get-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `list<string>` | yes | The API name of the module whose records you want to fetch. |
| `fields` | query | `string` | yes | Comma-separated field API names to include in the response. |
| `sort_by` | query | `string` | no | Field API name to sort the returned records by. |
| `sort_order` | query | `list<string>` | no | Sort direction for the requested records. Accepted values: `asc`, `desc`. |
| `approved` | query | `list<string>` | no | Choose whether to fetch only approved, only unapproved, or both record sets. Accepted values: `approved`, `both`, `unapproved`. |
| `cvid` | query | `string` | no | Custom view ID to restrict the returned records. |
| `page_token` | query | `string` | no | Token used to continue pagination from a previous response. |
