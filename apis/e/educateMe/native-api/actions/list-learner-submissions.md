# List Learner Submissions with EducateMe

Lists learner submissions for a course in EducateMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:id/assignments-submissions`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [List Learner Submissions](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2b5bae16ba8f4883b049b83e3c8b03e9)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `status[]` | query | `array<string>` | no |
| `student_emails` | query | `string` | no |
| `activityId` | query | `string` | no |
| `last_updated_items` | query | `number` | no |
