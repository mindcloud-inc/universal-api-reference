# Update Highlight with Readwise

Updates an existing highlight in Readwise.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/highlights/:highlightId/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Update Highlight](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlightId` | path | `number` | yes | The Readwise highlight ID to update. |
| `text` | body | `string` | no | The updated highlight text. |
| `note` | body | `string` | no | Annotation note attached to the specific highlight. |
| `color` | body | `string` | no | Highlight color tag. |
| `location` | body | `string` | no | Highlight location in the source text. |
| `url` | body | `string` | no | Unique URL of the specific highlight. |
