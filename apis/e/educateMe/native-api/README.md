# EducateMe: Native API Reference

A consolidated summary of EducateMe's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f
- **API base URL:** `https://api.educate-me.co`

## Authentication

### API Key

Connect with an EducateMe API key from General settings -> API Access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://help.educate-me.co/en/articles/8795762-api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `result`.

## Pagination

Use `perPage` in the query string to set the page size (default 10). Use `currentPage` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /activities` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2b7bb560440146b19c99f8c3a33904b4) |
| [Create Course](actions/create-course.md) | `POST /courses` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#7e8cb7da90ea4766a12238dfe9f8c74d) |
| [Create Learner Session](actions/create-learner-session.md) | `POST /students/:email/sessions` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#95f11204f20e4a9eb5aa6e5b7f31ec6e) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2bf447e2efaa80589d3fe71414c60fff) |
| [Delete Activity](actions/delete-activity.md) | `DELETE /activities/:id` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#04859b6ad052427dadcf6cca518b49da) |
| [Delete Course](actions/delete-course.md) | `DELETE /courses/:id` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#a99cebcdd43a4eb6926170e867b728d1) |
| [Delete Learner from Workspace](actions/delete-learner-from-workspace.md) | `DELETE /students/:email` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#80d7f753e1924f21bbb71b07d91d75d4) |
| [Export Feedback Notes](actions/export-feedback-notes.md) | `GET /courses/feedback` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#145447e2efaa8008bdd7fecd0400844e) |
| [Export Feedback Reactions](actions/export-feedback-reactions.md) | `GET /courses/feedback_reactions` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#233447e2efaa80bfbd30f5247be406a6) |
| [Invite Learner to Course](actions/invite-learner-to-course.md) | `POST /courses/:courseId/students` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#696222b841654e908683875d823ab2b4) |
| [Invite Learner to Many Courses](actions/invite-learner-to-many-courses.md) | `POST /courses/invite` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#f71a578ecd1c408a8d8232ceb7ffec10) |
| [List Course Activities](actions/list-course-activities.md) | `GET /courses/:id/lessons` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#e2515ce4dfd240caa2f9cf31bf60f093) |
| [List Course Schedules](actions/list-course-schedules.md) | `GET /courses/:courseId/schedules` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#9f2290b158a34d74885ccb2dbc290e10) |
| [List Course Transcripts](actions/list-course-transcripts.md) | `GET /courses/:id/transcripts` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#249447e2efaa80328f2eedc53a2698ed) |
| [List Courses](actions/list-courses.md) | `GET /courses` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f) |
| [List Learner Submissions](actions/list-learner-submissions.md) | `GET /courses/:id/assignments-submissions` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2b5bae16ba8f4883b049b83e3c8b03e9) |
| [List Learners' Assignments by Course](actions/list-learners-assignments-by-course.md) | `GET /courses/:courseId/students-assignments` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#f450767bb06c4942b5e783b5223a8f2c) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2bf447e2efaa804f80dace3d8594cd9b) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f) |
| [Remove Learner from Course](actions/remove-learner-from-course.md) | `POST /courses/:courseId/students/unassign` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#98ca2b719230472da8fd7bc65f5031d1) |
| [Schedule Event Activities for Course](actions/schedule-event-activities-for-course.md) | `POST /courses/:courseId/schedule-events` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#1bf447e2efaa8031a82ef9f1f2daa11d) |
| [Submit Assignment for Learner](actions/submit-assignment-for-learner.md) | `POST /assignments/submit` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#34c4ce8f275a4e838f299f911157f351) |
| [Update Activity](actions/update-activity.md) | `POST /activities/:activityId/update` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#7dd53470f51345a9bf6ee8da8f141fdc) |
| [Update Learner Suspension Status](actions/update-learner-suspension-status.md) | `POST /students/:email` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#7f8ba3abfef0443fb86e07842361b6d8) |
| [Update User](actions/update-user.md) | `POST /users/:email` | [docs](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2c3447e2efaa80b39a46e8ef1561e687) |
