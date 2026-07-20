# List Merge Templates with Zoho Writer

Retrieves merge templates from Zoho Writer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/documents`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [List Merge Templates](https://www.zoho.com/writer/help/api/v1/get-merge-templates.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Limit results to all templates, templates shared to you, or templates you own. |
| `sortby` | query | `string` | no | Sort merge templates by created time, modified time, or name. |
| `sort_order_by` | query | `string` | no | Choose ascending or descending sort order. |
