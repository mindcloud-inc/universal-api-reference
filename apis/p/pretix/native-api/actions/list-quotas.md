# List Quotas with pretix

Retrieves quotas from a pretix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/quotas/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [List Quotas](https://docs.pretix.eu/dev/api/resources/quotas.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
