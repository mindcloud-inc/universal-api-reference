# Track Event with SMASHSEND Email Marketing

Tracks a single contact event in SMASHSEND.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events`
- **Base URL:** `https://api.smashsend.com`
- **Official documentation:** [Track Event](https://smashsend.com/docs/api/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Event name to track, for example user.signup or purchase.completed. |
| `identify` | body | `object` | yes | Identity payload for the event, including at least the contact email. |
| `messageId` | body | `string` | no | Optional custom message ID for deduplication. |
| `properties` | body | `object` | no | Optional event properties object. |
| `timestamp` | body | `date` | no | Optional ISO 8601 timestamp for the event. |
