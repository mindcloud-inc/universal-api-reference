# Update Discussion Topic with Instructure

Updates an existing discussion topic in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/:course_id/discussion_topics/:topic_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Discussion Topic](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `topic_id` | path | `string` | yes | The Canvas discussion topic ID. |
| `title` | body | `string` | no | Discussion title. |
| `message` | body | `string` | no | Discussion body. |
| `published` | body | `boolean` | no | Publish immediately. |
