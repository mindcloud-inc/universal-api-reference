# Delete Discussion Topic with Instructure

Deletes a discussion topic from Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/courses/:course_id/discussion_topics/:topic_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Delete Discussion Topic](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `topic_id` | path | `string` | yes | The Canvas discussion topic ID. |
