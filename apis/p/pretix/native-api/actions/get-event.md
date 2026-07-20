# Get Event with pretix

Retrieves an event from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Event](https://docs.pretix.eu/dev/api/resources/events.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
