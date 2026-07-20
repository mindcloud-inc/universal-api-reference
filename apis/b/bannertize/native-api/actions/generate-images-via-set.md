# Generate Images via Set with Bannertize

Creates multiple images from a set in Bannertize.

## Endpoint

- **Method:** `POST`
- **Path:** `set`
- **Base URL:** `https://api.bannertize.com/v1`
- **Official documentation:** [Generate Images via Set](https://docs.bannertize.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifications[]` | body | `array<object>` | no | An array of Bannertize layer modifications to apply to the set. |
| `set` | body | `string` | yes | The Bannertize set UID to render. |
