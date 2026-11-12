# Replace All Text with Google Slides

Replaces every occurrence of a text or pattern across the presentation, useful for filling template placeholders.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Replace All Text](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#ReplaceAllTextRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].replaceAllText.containsText` | body | `object` | no | — |
| `containsText.text` | body | `string` | yes | The text to search for in shapes and tables. |
| `containsText.matchCase` | body | `boolean` | no | Whether the search is case sensitive. |
| `containsText.searchByRegex` | body | `boolean` | no | Treat the search text as a regular expression; backslashes must be escaped. |
| `requests[0].replaceAllText.replaceText` | body | `string` | yes | Text that replaces each match. |
| `requests[0].replaceAllText.pageObjectIds[]` | body | `array<string>` | no | Limit the change to these slide IDs. Applies to all slides when empty. |
