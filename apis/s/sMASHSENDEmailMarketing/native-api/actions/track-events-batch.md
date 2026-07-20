# Track Events Batch with SMASHSEND Email Marketing

Tracks multiple contact events in SMASHSEND in one batch.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events/batch`
- **Base URL:** `https://api.smashsend.com`
- **Official documentation:** [Track Events Batch](https://smashsend.com/docs/api/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<object>` | yes | Array of event payloads to send in a single batch request. |
