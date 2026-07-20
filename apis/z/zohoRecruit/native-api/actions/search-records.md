# Search Records with Zoho Recruit

Finds records in Zoho Recruit by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName/search`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Search Records](https://www.zoho.com/recruit/developer-guide/apiv2/search-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name to search. |
| `criteria` | query | `string` | no | Criteria expression to search records by field values. |
| `email` | query | `string` | no | Search records by email across the module email fields. |
| `phone` | query | `string` | no | Search records by phone number across the module phone fields. |
| `word` | query | `string` | no | Search records globally by a word match. |
| `page` | query | `number` | no | Page number of search results to fetch. |
| `per_page` | query | `number` | no | Maximum number of search results to fetch per page. |
| `converted` | query | `string` | no | Whether to fetch converted, non-converted, or all converted states. Accepted values: `both`, `false`, `true`. |
| `approved` | query | `string` | no | Whether to fetch approved, unapproved, or all approval states. Accepted values: `both`, `false`, `true`. |
