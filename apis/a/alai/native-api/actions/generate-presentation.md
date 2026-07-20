# Generate Presentation with Alai

Creates an async presentation generation in Alai from text input.

## Endpoint

- **Method:** `POST`
- **Path:** `/generations`
- **Base URL:** `https://slides-api.getalai.com/api/v1`
- **Official documentation:** [Generate Presentation](https://docs.getalai.com/api/generations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input_text` | body | `string` | yes | Source text used to generate the presentation. |
| `presentation_options.title` | body | `string` | yes | Title for the generated presentation. |
| `presentation_options.slide_range` | body | `string` | no | Requested slide count range like 2-3 or 6-10. |
| `presentation_options.theme_id` | body | `string` | no | Theme identifier returned by Get Themes. |
| `export_formats[]` | body | `array<string>` | no | Requested export formats like link, pdf, or ppt. |
| `image_ids[]` | body | `array<string>` | no | Uploaded image identifiers to include in generation. |
