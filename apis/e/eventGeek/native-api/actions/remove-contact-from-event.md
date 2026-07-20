# Remove Contact From Event with EventGeek

Removes a contact from an event in EventGeek.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/events/:event_id/contacts/:contact_id`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [Remove Contact From Event](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Circa contact identifier. |
| `event_id` | path | `string` | yes | Circa event identifier. |
