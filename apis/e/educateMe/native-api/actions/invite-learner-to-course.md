# Invite Learner to Course with EducateMe

Invites a learner to a course in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:courseId/students`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Invite Learner to Course](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#696222b841654e908683875d823ab2b4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | Course ID. |
| `email` | body | `string` | yes | Learner email. |
| `name` | body | `string` | yes | Learner name. |
| `note` | body | `string` | no | Optional learner note. |
| `tagsIds[]` | body | `array<string>` | no | Optional tag IDs. |
| `tagNames[]` | body | `array<string>` | no | Optional tag names. |
| `withoutConfirmation` | query | `boolean` | no | Auto-confirm learner account when true. |
