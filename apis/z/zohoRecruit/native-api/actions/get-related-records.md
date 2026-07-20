# Get Related Records with Zoho Recruit

Retrieves related records from Zoho Recruit.

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName/:recordId/:relatedModule`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Get Related Records](https://www.zoho.com/recruit/developer-guide/apiv2/get-related-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name that owns the related records. |
| `recordId` | path | `string` | yes | The unique ID of the base Zoho Recruit record. |
| `relatedModule` | path | `string` | yes | The related list API name, such as Attachments or Notes. |
| `ids` | query | `string` | no | Comma-separated related record IDs to filter the related-record response. Send multiple values as a string separated by `,`. |
| `fields` | query | `string` | no | Comma-separated field API names to include in the related-record response. |
| `page` | query | `number` | no | Page number of related records to fetch. |
| `per_page` | query | `number` | no | Maximum number of related records to fetch per page. |
| `sort_by` | query | `string` | no | Field API name to sort the related records by. |
| `sort_order` | query | `string` | no | Sort order to apply to the selected sort field. Accepted values: `asc`, `desc`. |
