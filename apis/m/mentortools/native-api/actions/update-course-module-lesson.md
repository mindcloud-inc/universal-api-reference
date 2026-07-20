# Update Course Module Lesson with Mentortools

Updates an existing course module lesson in Mentortools.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/v1/lessons/:lesson_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Update Course Module Lesson](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lesson_id` | path | `number` | yes | The lesson ID. |
| `lesson_type` | body | `string` | yes | Type of the lesson. |
| `title` | body | `string` | yes | Title of the lesson. |
| `is_active` | body | `boolean` | yes | Whether the lesson is active. |
| `is_published` | body | `boolean` | yes | Whether the lesson is published. |
| `mandatory` | body | `boolean` | yes | Whether the lesson is mandatory. |
| `order` | body | `number` | yes | Order of the lesson. |
| `content_blocks[].id` | body | `number` | no | — |
| `content_blocks[].block_type` | body | `string` | yes | — |
| `content_blocks[].order` | body | `number` | yes | — |
| `content_blocks[].is_expanded` | body | `boolean` | no | — |
| `content_blocks[].content.payload` | body | `string` | no | — |
| `attached_files[].order` | body | `number` | yes | — |
| `attached_files[].file_id` | body | `number` | yes | — |
