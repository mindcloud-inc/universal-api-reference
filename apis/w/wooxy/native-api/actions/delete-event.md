# Delete Event with Wooxy

Deletes an existing event from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/custom-event/remove`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Delete Event](https://wooxy.com/api-documentation/events/remove-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | no | An array of Wooxy event IDs to delete. |
| `names[]` | body | `array<string>` | no | An array of Wooxy event names to delete. |
