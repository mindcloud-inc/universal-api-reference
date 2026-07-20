# Use A Custom Font with Creatomate

Creates a render that uses a custom font.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Use A Custom Font](https://creatomate.com/docs/api/quick-start/use-a-custom-font)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fontFamily` | body | `string` | yes | Font family name to register and use in the render. |
| `regularFontUrl` | body | `string` | yes | URL for the regular font file. |
| `italicFontUrl` | body | `string` | no | Optional URL for the italic font file. |
| `headlineText` | body | `string` | yes | Primary text rendered with the custom font. |
| `subheadlineText` | body | `string` | no | Optional secondary text line rendered below the headline. |
