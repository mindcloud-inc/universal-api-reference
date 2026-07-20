# Create Lesson with TrainerCentral

Creates a lesson in TrainerCentral.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [Create Lesson](https://help.trainercentral.com/portal/en/kb/articles/create-a-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session.name` | body | `string` | yes | The lesson name. |
| `session.courseId` | body | `string` | yes | The course ID the lesson belongs to. |
| `session.sectionId` | body | `string` | yes | The chapter ID the lesson belongs to. |
