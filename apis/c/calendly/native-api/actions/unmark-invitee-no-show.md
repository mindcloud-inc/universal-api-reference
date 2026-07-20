# Unmark Invitee No Show with Calendly

Removes a no-show mark from a Calendly invitee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/invitee_no_shows/:invitee_no_show_uuid`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Unmark Invitee No Show](https://developer.calendly.com/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invitee_no_show_uuid` | path | `string` | yes | Invitee no-show UUID. |
