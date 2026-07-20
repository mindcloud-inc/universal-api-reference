# Update Page with Instructure

Updates an existing page in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/:course_id/pages/:page_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Page](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `page_id` | path | `string` | yes | The Canvas page identifier. |
| `wiki_page[title]` | body | `string` | no | Page title. |
| `wiki_page[body]` | body | `string` | no | Page body HTML or text. |
