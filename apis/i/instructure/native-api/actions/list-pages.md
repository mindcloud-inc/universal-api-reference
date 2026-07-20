# List Pages with Instructure

Retrieves pages from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/pages`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Pages](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
