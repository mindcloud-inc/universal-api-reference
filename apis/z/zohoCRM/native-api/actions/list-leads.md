# List Leads with Zoho CRM

Retrieves lead records from Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Leads`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [List Leads](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | yes | Comma-separated lead field API names to return. Send multiple values as a string separated by `,`. |
| `ids` | query | `string` | no | Comma-separated lead record IDs to retrieve. Send multiple values as a string separated by `,`. |
| `converted` | query | `list<string>` | no | Whether to return converted, non-converted, or both lead records. Accepted values: `both`, `false`, `true`. |
| `cvid` | query | `string` | no | Custom view ID to fetch leads from a saved view. |
