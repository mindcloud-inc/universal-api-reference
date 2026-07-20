# List Learners' Assignments by Course with EducateMe

Lists learner assignments for a course in EducateMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:courseId/students-assignments`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [List Learners' Assignments by Course](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#f450767bb06c4942b5e783b5223a8f2c)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `courseId` | path | `string` | yes |
| `status` | query | `string` | no |
| `student_email` | query | `string` | no |
