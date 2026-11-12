# Create Slide with Google Slides

Adds a new slide to a presentation, optionally at a position and with a predefined or existing layout.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Create Slide](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#CreateSlideRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].createSlide.insertionIndex` | body | `number` | no | Zero-based position for the new slide. Appends to the end when omitted. |
| `requests[0].createSlide.slideLayoutReference` | body | `object` | no | — |
| `slideLayoutReference.predefinedLayout` | body | `list<string>` | no | Predefined layout from the current master. Not every master contains every layout. Accepted values: `BIG_NUMBER`, `BLANK`, `CAPTION_ONLY`, `MAIN_POINT`, `ONE_COLUMN_TEXT`, `PREDEFINED_LAYOUT_UNSPECIFIED`, `SECTION_HEADER`, `SECTION_TITLE_AND_DESCRIPTION`, `TITLE`, `TITLE_AND_BODY`, `TITLE_AND_TWO_COLUMNS`, `TITLE_ONLY`. |
| `slideLayoutReference.layoutId` | body | `string` | no | Object ID of a layout in the presentation. Use instead of Predefined Layout. |
| `requests[0].createSlide.objectId` | body | `string` | no | Optional custom ID for the new object: 5-50 characters, starting with a letter, digit or underscore. Generated when omitted. |
| `requests[0].createSlide.placeholderIdMappings[]` | body | `array<object>` | no | Assign your own object IDs to layout placeholders created on the slide, so later actions can target them. |
| `placeholderIdMappings[].objectId` | body | `string` | no | Custom ID for the placeholder created on the slide. |
| `placeholderIdMappings[].layoutPlaceholder` | body | `object` | no | — |
| `placeholderIdMappings[].layoutPlaceholder.type` | body | `list<string>` | no | Accepted values: `BODY`, `CENTERED_TITLE`, `CHART`, `CLIP_ART`, `DATE_AND_TIME`, `DIAGRAM`, `FOOTER`, `HEADER`, `MEDIA`, `NONE`, `OBJECT`, `PICTURE`, `SLIDE_IMAGE`, `SLIDE_NUMBER`, `SUBTITLE`, `TABLE`, `TITLE`. |
| `placeholderIdMappings[].layoutPlaceholder.index` | body | `number` | no | — |
| `placeholderIdMappings[].layoutPlaceholderObjectId` | body | `string` | no | Object ID of the layout placeholder. Use instead of Layout Placeholder. |
