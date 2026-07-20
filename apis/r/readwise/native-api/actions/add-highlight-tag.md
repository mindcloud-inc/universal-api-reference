# Add Highlight Tag with Readwise

Creates a new tag for a Readwise highlight.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/highlights/:highlightId/tags/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Add Highlight Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlightId` | path | `number` | yes | The Readwise highlight ID to tag. |
| `name` | body | `string` | yes | The tag name to add to the highlight. Maximum length: 127. |
