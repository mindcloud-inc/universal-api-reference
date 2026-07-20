# Get Organizer Settings with pretix

Retrieves organizer settings from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/settings/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Get Organizer Settings](https://docs.pretix.eu/dev/api/resources/organizers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
