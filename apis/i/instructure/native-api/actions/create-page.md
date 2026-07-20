# Create Page with Instructure

Creates a new page in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:course_id/pages`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Page](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `wiki_page[title]` | body | `string` | yes | Page title. |
| `wiki_page[body]` | body | `string` | no | Page body HTML or text. |
