# Get Organizer with pretix

Retrieves an organizer from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Organizer](https://docs.pretix.eu/dev/api/resources/organizers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
