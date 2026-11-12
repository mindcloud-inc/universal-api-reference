# Batch Update Presentation with Google Slides

Applies one or more batch update requests to a presentation in a single atomic call. Use the dedicated actions for common single changes.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Batch Update Presentation](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[]` | body | `array<object>` | yes | Batch update requests, each an object with one request type (for example createSlide, insertText, replaceAllText). The Request union has 49 request types, so items are passed as raw JSON. |
| `writeControl` | body | `object` | no | Optional conditional-write settings. |
| `writeControl.requiredRevisionId` | body | `string` | no | Only apply the update when this is still the latest revision of the presentation. |
