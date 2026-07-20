# Get Sub Event with pretix

Retrieves a sub-event from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/subevents/:subevent/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Sub Event](https://docs.pretix.eu/dev/api/resources/subevents.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `subevent` | path | `string` | yes | pretix sub-event ID. |
