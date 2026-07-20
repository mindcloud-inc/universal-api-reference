# Save Document To Reader with Readwise

Saves a document to Readwise Reader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/save/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Save Document To Reader](https://readwise.io/reader_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The document's unique URL. |
| `html` | body | `string` | no | The document content in valid HTML. |
| `should_clean_html` | body | `boolean` | no | Automatically clean provided HTML and parse metadata. |
| `title` | body | `string` | no | Override title for the document. |
| `author` | body | `string` | no | Override author for the document. |
| `summary` | body | `string` | no | Summary of the document. |
| `published_date` | body | `date` | no | ISO 8601 datetime when the document was published. |
| `image_url` | body | `string` | no | Cover image URL for the document. |
| `location` | body | `string` | no | Initial location for the document. |
| `category` | body | `string` | no | Category for the saved document. |
| `saved_using` | body | `string` | no | Source of the document. |
| `tags[]` | body | `array<string>` | no | List of tag strings for the document. |
| `notes` | body | `string` | no | Top-level note for the document. |
