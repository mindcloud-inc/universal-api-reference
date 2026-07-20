# List Item Variations with pretix

Retrieves item variations from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/items/:item/variations/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Item Variations](https://docs.pretix.eu/dev/api/resources/item_variations.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `item` | path | `string` | yes | pretix item ID. |
