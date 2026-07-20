# Send Message with Vestaboard

Sends a new message to Vestaboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://cloud.vestaboard.com`
- **Official documentation:** [Send Message](https://docs.vestaboard.com/docs/read-write-api/endpoints/#send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | no | Plain-text message to show on the Vestaboard. |
| `characters[]` | body | `array<array>` | no | Two-dimensional array of Vestaboard character codes. |
| `forced` | body | `boolean` | no | Override quiet hours when true. |
