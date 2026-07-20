# List Items with pretix

Retrieves items from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/items/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Items](https://docs.pretix.eu/dev/api/resources/items.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
