# List Discussion Topics with Instructure

Retrieves discussion topics from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/discussion_topics`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Discussion Topics](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
