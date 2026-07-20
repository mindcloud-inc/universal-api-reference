# Invite Learner to Many Courses with EducateMe

Invites a learner to multiple courses in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/invite`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Invite Learner to Many Courses](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#f71a578ecd1c408a8d8232ceb7ffec10)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Learner email. |
| `name` | body | `string` | yes | Learner name. |
| `courses_ids[]` | body | `array<string>` | yes | Course IDs to invite the learner to. |
| `note` | body | `string` | no | Optional learner note. |
| `tagsIds[]` | body | `array<string>` | no | Optional tag IDs. |
| `tagNames[]` | body | `array<string>` | no | Optional tag names. |
| `customProperties[]` | body | `array<object>` | no | Optional custom properties for the learner. |
| `withoutConfirmation` | query | `boolean` | no | Auto-confirm learner account when true. |
