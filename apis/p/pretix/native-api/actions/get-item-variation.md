# Get Item Variation with pretix

Retrieves an item variation from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/items/:item/variations/:variation/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Item Variation](https://docs.pretix.eu/dev/api/resources/item_variations.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `item` | path | `string` | yes | pretix item ID. |
| `variation` | path | `string` | yes | pretix item variation ID. |
