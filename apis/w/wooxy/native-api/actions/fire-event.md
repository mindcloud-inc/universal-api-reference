# Fire Event with Wooxy

Fires a custom event in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/custom-event/fire`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Fire Event](https://wooxy.com/api-documentation/events/fire-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | The verified sender domain name from your Wooxy account. |
| `customEvent` | body | `string` | yes | The Wooxy event ID or event name to fire. |
| `contact` | body | `string` | yes | The recipient email, user ID, or phone number already stored in the default contact list. |
| `dateTime` | body | `string` | no | Optional event occurrence time in ISO8601 format. |
| `ipAddress` | body | `string` | no | Optional IPv4 address associated with the event. |
| `userAgent` | body | `string` | no | Optional user agent string. |
