# List scheduled SMS by created date range with Webex Interact

Finds scheduled SMS requests in Webex Interact by created date range.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/v1/scheduled`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [List scheduled SMS by created date range](https://docs.webexinteract.com/reference/scheduled-messages-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.id` | body | `string` | no | Campaign or API SMS request ID to retrieve. |
| `filter.name` | body | `string` | no | Fuzzy match search on the campaign or API request name. |
| `filter.scheduled_at_end` | body | `date` | no | End of scheduled-at date range. |
| `filter.scheduled_at_start` | body | `date` | no | Start of scheduled-at date range. |
| `page.page_number` | body | `string` | no | Page number to return. |
| `page.page_size` | body | `string` | no | Number of scheduled requests per page. |
| `sort.sort_by` | body | `string` | no | Scheduled SMS sort field such as created_at, updated_at, scheduled_at, name, or status. |
| `sort.sort_order` | body | `string` | no | Sort order, ASC or DESC. |
| `filter.created_at_start` | body | `date` | yes | Start of created-at date range. Required unless ID or scheduled-at range is supplied. |
| `filter.created_at_end` | body | `date` | yes | End of created-at date range. Required with created-at start. |
| `filter.status` | body | `list<string>` | no | Statuses to return, such as SCHEDULED, SENT, ERROR, DELETED, or IN_PROGRESS. |
| `filter.request_types` | body | `list<string>` | no | Request types to return: CAMPAIGN and/or API. |
