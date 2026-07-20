# Get Check In List with pretix

Retrieves a check-in list from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/checkinlists/:list/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Check In List](https://docs.pretix.eu/dev/api/resources/checkinlists.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `list` | path | `string` | yes | pretix check-in list ID. |
