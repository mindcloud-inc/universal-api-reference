# Get Event Settings with pretix

Retrieves event settings from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/settings/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Event Settings](https://docs.pretix.eu/dev/api/resources/events.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
