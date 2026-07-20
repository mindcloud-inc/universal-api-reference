# Search Organizer Orders with pretix

Searches orders across a pretix organizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/orders/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Search Organizer Orders](https://docs.pretix.eu/dev/api/resources/orders.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `search` | query | `string` | no | Search query for matching order names, emails, or companies. |
