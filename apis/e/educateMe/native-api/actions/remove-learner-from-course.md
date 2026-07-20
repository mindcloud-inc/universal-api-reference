# Remove Learner from Course with EducateMe

Removes a learner from a course in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:courseId/students/unassign`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Remove Learner from Course](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#98ca2b719230472da8fd7bc65f5031d1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | Course ID. |
| `email` | body | `string` | yes | Learner email. |
