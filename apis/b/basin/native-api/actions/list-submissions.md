# List Submissions with Basin

Retrieves submission records from Basin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/submissions`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [List Submissions](https://usebasin.com/api_docs/index.html)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | query | `string` | no | Retrieve submissions for a specific Basin form. Optional when using a Form API key. |
| `filter_by` | query | `string` | no | Filter submissions by new, spam, trash, or all. |
| `query` | query | `string` | no | Search submissions by query. |
| `order_by` | query | `string` | no | Order submissions by date_asc, date_desc, email_asc, or email_desc. |
| `date_range` | query | `string` | no | Filter submissions by date range in the format YYYY-MM-DD+to+YYYY-MM-DD. |
