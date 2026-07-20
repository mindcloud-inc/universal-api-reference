# Create Highlights with Readwise

Creates new highlights in the Readwise library.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/highlights/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Create Highlights](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlights[]` | body | `array<object>` | yes | Array of highlight objects to create or update. |
| `highlights[].text` | body | `string` | yes | The highlight text. |
| `highlights[].title` | body | `string` | no | Title of the source book, article, or podcast. |
| `highlights[].author` | body | `string` | no | Author of the source book, article, or podcast. |
| `image_url` | body | `string` | no | Cover image URL for the source. |
| `source_url` | body | `string` | no | URL of the source article or podcast. |
| `source_type` | body | `string` | no | A meaningful unique identifier for your app. |
| `highlights[].category` | body | `string` | no | Category for the highlight source. |
| `highlights[].note` | body | `string` | no | Annotation note attached to the highlight. |
| `highlights[].location` | body | `number` | no | Highlight location in the source text. |
| `location_type` | body | `string` | no | How the highlight location should be interpreted. |
| `highlighted_at` | body | `string` | no | ISO 8601 datetime when the highlight was taken. |
| `highlight_url` | body | `string` | no | Unique URL of the specific highlight. |
