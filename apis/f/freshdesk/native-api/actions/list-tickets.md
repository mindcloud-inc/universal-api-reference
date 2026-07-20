# List Tickets with Freshdesk

Retrieves a list of tickets from Freshdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [List Tickets](https://developers.freshdesk.com/api/#list_all_tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `list<string>` | no | Predefined Freshdesk ticket filter (new_and_my_open, watching, spam, deleted). Accepted values: `deleted`, `new_and_my_open`, `spam`, `watching`. |
| `include` | query | `string` | no | Embed additional fields (stats, requester, description). |
