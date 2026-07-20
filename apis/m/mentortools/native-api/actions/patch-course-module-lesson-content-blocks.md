# Patch Course Module Lesson Content Blocks with Mentortools

Updates lesson content blocks in Mentortools, creating new ones when needed.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/courses/v1/lessons/:lesson_id/content_blocks`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Patch Course Module Lesson Content Blocks](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lesson_id` | path | `number` | yes | The lesson ID. |
| `content_blocks[].id` | body | `number` | no | — |
| `content_blocks[].block_type` | body | `string` | yes | — |
| `content_blocks[].order` | body | `number` | yes | — |
| `content_blocks[].is_expanded` | body | `boolean` | no | — |
| `content_blocks[].content.payload` | body | `string` | no | — |
