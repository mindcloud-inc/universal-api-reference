# Delete Page with Instructure

Deletes a page from Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/courses/:course_id/pages/:page_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Delete Page](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `page_id` | path | `string` | yes | The Canvas page identifier. |
