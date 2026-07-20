# Create ManyChat Response Image with NiftyImages

Creates a ManyChat response image in NiftyImages.

## Endpoint

- **Method:** `POST`
- **Path:** `/ManyChat`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Create ManyChat Response Image](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Url` | body | `string` | yes | NiftyImages URL that should be formatted. |
| `Variables[]` | body | `array<object>` | no | Variables array. |
| `Variables[].Name` | body | `string` | no | Variable or placeholder name. |
| `Variables[].Value` | body | `string` | no | Value appended to the final result. |
