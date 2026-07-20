# List Ticket Groups with Checkout Page

Retrieves ticket groups from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:pageId/ticket-groups`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [List Ticket Groups](https://checkoutpage.com/docs/api/v1/events/ticket-groups/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the event page. |
