# List Invoices with pretix

Retrieves invoices from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/invoices/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Invoices](https://docs.pretix.eu/dev/api/resources/invoices.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
