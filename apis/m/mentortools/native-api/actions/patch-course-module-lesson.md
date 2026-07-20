# Patch Course Module Lesson with Mentortools

Updates part of an existing course module lesson in Mentortools.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/courses/v1/lessons/:lesson_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Patch Course Module Lesson](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lesson_id` | path | `number` | yes | The lesson ID. |
| `title` | body | `string` | no | Title of the lesson. |
