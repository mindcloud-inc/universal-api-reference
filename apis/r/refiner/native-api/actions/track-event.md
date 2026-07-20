# Track Event with Refiner

Tracks a user event in Refiner.

## Endpoint

- **Method:** `POST`
- **Path:** `/track-event`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Track Event](https://refiner.io/docs/api/#track-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | The user ID to identify the contact for this event. |
| `email` | body | `string` | no | Use an email address when you do not have the user ID. |
| `event` | body | `string` | yes | The name of the event to track. |
