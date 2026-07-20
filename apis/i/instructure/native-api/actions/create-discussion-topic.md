# Create Discussion Topic with Instructure

Creates a new discussion topic in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:course_id/discussion_topics`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Discussion Topic](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `title` | body | `string` | yes | Discussion title. |
| `message` | body | `string` | no | Discussion body. |
| `published` | body | `boolean` | no | Publish immediately. |
