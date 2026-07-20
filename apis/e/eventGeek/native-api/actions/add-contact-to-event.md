# Add Contact To Event with EventGeek

Adds a contact to an event in EventGeek.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:event_id/contacts`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [Add Contact To Event](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `string` | yes | Contact to add to the event. |
| `event_id` | path | `string` | yes | Circa event identifier. |
