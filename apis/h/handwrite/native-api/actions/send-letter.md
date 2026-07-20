# Send Letter with Handwrite

Sends a handwritten letter through Handwrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://api.handwrite.io/v1`
- **Official documentation:** [Send Letter](https://documentation.handwrite.io/#send-a-letter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Letter body text. Handwrite documents a maximum of 320 characters. |
| `handwriting` | body | `string` | yes | The handwriting ID to use for the letter. |
| `card` | body | `string` | yes | The stationery or card ID to use for the letter. |
| `recipients[]` | body | `array<object>` | yes | Array of recipient objects. Each recipient should include address fields such as firstName, lastName, street1, city, state, and zip. |
| `from` | body | `object` | no | Optional return-address object with firstName, lastName, street1, street2, city, state, and zip. |
