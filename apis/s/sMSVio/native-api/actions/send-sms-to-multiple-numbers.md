# Send SMS to Multiple Numbers with SMSVio

## Endpoint

- **Method:** `POST`
- **Path:** `/services/send/`
- **Base URL:** `https://gate.smsvio.cz`
- **Official documentation:** [Send SMS to Multiple Numbers](https://www.smsvio.cz/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages` | body | `string<object>` | yes | JSON string array of {number, message} objects to send |
| `useAvailable` | body | `boolean` | no | Prefer an available device for delivery |
| `devices` | body | `string` | no | Optional device identifiers to use for delivery |
