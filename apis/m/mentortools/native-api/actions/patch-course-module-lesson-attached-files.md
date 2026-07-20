# Patch Course Module Lesson Attached Files with Mentortools

Updates lesson attached files in Mentortools, creating new ones when needed.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/courses/v1/lessons/:lesson_id/attached_files`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Patch Course Module Lesson Attached Files](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lesson_id` | path | `number` | yes | The lesson ID. |
| `attached_files[].id` | body | `number` | no | — |
| `attached_files[].order` | body | `number` | yes | — |
| `attached_files[].file_id` | body | `number` | yes | — |
