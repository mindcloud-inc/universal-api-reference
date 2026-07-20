# Create Course with TrainerCentral

Creates a new course in TrainerCentral.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [Create Course](https://help.trainercentral.com/portal/en/kb/articles/create-course-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course.courseName` | body | `string` | yes | The name of the course to create. |
| `course.subTitle` | body | `string` | yes | A short subtitle for the course. |
| `course.description` | body | `string` | yes | A short course description. |
