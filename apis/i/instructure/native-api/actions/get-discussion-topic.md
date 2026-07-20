# Get Discussion Topic with Instructure

Retrieves a discussion topic from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/discussion_topics/:topic_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Discussion Topic](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics_api.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `topic_id` | path | `string` | yes | The Canvas discussion topic ID. |
