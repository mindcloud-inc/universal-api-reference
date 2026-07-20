# Get Item with pretix

Retrieves an item from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/items/:item/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Item](https://docs.pretix.eu/dev/api/resources/items.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `item` | path | `string` | yes | pretix item ID. |
