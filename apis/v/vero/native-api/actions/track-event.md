# Track Event with Vero

Tracks an event record in Vero.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/events/track`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Track Event](https://help.getvero.com/api-reference/events/track)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity` | body | `object` | yes | User identity object containing id and or email for the event subject. |
| `event_name` | body | `string` | yes | The name of the event to track. |
| `data` | body | `object` | no | Optional event properties. |
| `extras` | body | `object` | no | Optional Vero-specific metadata like source or created_at. |
