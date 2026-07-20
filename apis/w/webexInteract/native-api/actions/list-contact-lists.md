# List contact lists with Webex Interact

Retrieves contact lists from Webex Interact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/v1/lists`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [List contact lists](https://docs.webexinteract.com/reference/lists-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Case-insensitive partial list name search. |
| `page_number` | query | `string` | no | Page number to return. |
| `page_size` | query | `string` | no | Number of lists per page. |
| `sort_by` | query | `string` | no | Sort field: updated_at, created_at, or name. |
| `sort_order` | query | `string` | no | Sort order: ASC or DESC. |
