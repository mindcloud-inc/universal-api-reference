# Get Quota Availability with pretix

Retrieves quota availability from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/quotas/:quota/availability/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Quota Availability](https://docs.pretix.eu/dev/api/resources/quotas.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `quota` | path | `string` | yes | pretix quota ID. |
