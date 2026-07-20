# List Records with Zoho Recruit

Retrieves records from a Zoho Recruit module.

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [List Records](https://www.zoho.com/recruit/developer-guide/apiv2/get-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name whose records you want to list. |
| `fields` | query | `string` | no | Comma-separated field API names to include in the list response. |
| `page` | query | `number` | no | Page number of records to fetch. |
| `per_page` | query | `number` | no | Maximum number of records to fetch per page. |
| `sort_by` | query | `string` | no | Field API name to sort the list by. |
| `sort_order` | query | `string` | no | Sort order to apply to the selected sort field. Accepted values: `asc`, `desc`. |
| `converted` | query | `string` | no | Whether to fetch converted, non-converted, or all converted states. Accepted values: `both`, `false`, `true`. |
| `approved` | query | `string` | no | Whether to fetch approved, unapproved, or all approval states. Accepted values: `both`, `false`, `true`. |
