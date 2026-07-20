# List scheduled SMS by scheduled date range with Webex Interact

Finds scheduled SMS requests in Webex Interact by scheduled date range.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/v1/scheduled`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [List scheduled SMS by scheduled date range](https://docs.webexinteract.com/reference/scheduled-messages-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.name` | body | `string` | no | Fuzzy match search on the campaign or API request name. |
| `filter.request_types` | body | `list<string>` | no | Optional request types to include. Send multiple values as a array. |
| `filter.scheduled_at_end` | body | `date` | yes | End of the scheduled send time range. |
| `filter.scheduled_at_start` | body | `date` | yes | Start of the scheduled send time range. |
| `filter.status` | body | `list<string>` | no | Optional scheduled request statuses to include. Send multiple values as a array. |
| `page.page_number` | body | `string` | no | Page number for scheduled SMS results. |
| `page.page_size` | body | `string` | no | Number of scheduled SMS results to return per page. |
| `sort.sort_by` | body | `string` | no | Scheduled SMS sort field such as created_at, updated_at, scheduled_at, name, or status. |
| `sort.sort_order` | body | `string` | no | Sort order, ASC or DESC. |
