# Create Invitee No Show with Calendly

Marks an invitee as a no-show in Calendly.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitee_no_shows`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Create Invitee No Show](https://developer.calendly.com/api-docs/cebd8c3170790-create-invitee-no-show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invitee` | body | `string` | yes | Invitee URI to mark as no-show. |
