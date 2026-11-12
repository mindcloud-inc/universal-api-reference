# Duplicate Object with Google Slides

Duplicates a slide or page element. A duplicated slide is placed right after the original; a duplicated element stays on the same slide.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Duplicate Object](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#DuplicateObjectRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].duplicateObject.objectId` | body | `string` | yes | Object ID of the slide or page element to duplicate. |
| `requests[0].duplicateObject.objectIds` | body | `object` | no | Map of original object IDs to the IDs to use for the duplicates, for example {"p": "slideCopy_01"}. Unmapped objects get random IDs. |
