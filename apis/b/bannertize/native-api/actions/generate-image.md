# Generate Image with Bannertize

Creates a new image from a template in Bannertize.

## Endpoint

- **Method:** `POST`
- **Path:** `image`
- **Base URL:** `https://api.bannertize.com/v1`
- **Official documentation:** [Generate Image](https://docs.bannertize.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifications[]` | body | `array<object>` | no | An array of Bannertize layer modifications to apply. |
| `template` | body | `string` | yes | The Bannertize template UID to render. |
