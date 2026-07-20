# TrainerCentral: Native API Reference

A consolidated summary of TrainerCentral's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://help.trainercentral.com/portal/en/kb/trainercentral/api-documentation
- **API base URL:** `{academyUrl}/api/v4/{orgId}`

## Authentication

### OAuth 2.0

### Credentials

- **Academy URL:** `academyUrl` · required · The full TrainerCentral academy URL, for example https://zylkeracademy.trainercentral.com
- **Org ID:** `orgId` · required · Your TrainerCentral academy org ID from the academy URL or portals API

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `TrainerCentral.portalapi.READ TrainerCentral.courseapi.READ TrainerCentral.courseapi.CREATE TrainerCentral.courseapi.UPDATE TrainerCentral.courseapi.DELETE TrainerCentral.sectionapi.CREATE TrainerCentral.sectionapi.UPDATE TrainerCentral.sectionapi.DELETE TrainerCentral.sessionapi.CREATE TrainerCentral.sessionapi.UPDATE TrainerCentral.sessionapi.DELETE TrainerCentral.talkapi.READ TrainerCentral.presenterapi.READ TrainerCentral.presenterapi.DELETE TrainerCentral.userapi.READ TrainerCentral.userapi.CREATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://help.trainercentral.com/portal/en/kb/articles/getting-started-oauth-token-generation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `si` in the query string as the record offset.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chapter](actions/create-chapter.md) | `POST /sections.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/create-a-chapter) |
| [Create Course](actions/create-course.md) | `POST /courses.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/create-course-api) |
| [Create Lesson](actions/create-lesson.md) | `POST /sessions.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/create-a-session) |
| [Create Live Lesson](actions/create-live-lesson.md) | `POST /sessions.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/create-a-session) |
| [Create Live Workshop](actions/create-live-workshop.md) | `POST /sessions.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/create-a-session) |
| [Get Learner Info](actions/get-learner-info.md) | `GET /fetchuserdetails.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/get-learner-info) |
| [Invite Learner to Course](actions/invite-learner-to-course.md) | `POST /addCourseAttendee.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/invite-learner-to-course-api) |
| [List Academy Learners](actions/list-academy-learners.md) | `GET /portalMembers.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/get-academy-learners-api) |
| [List Course Members](actions/list-course-members.md) | `GET /course/:courseId/courseMembers.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/how-do-i-get-coursememberid) |
| [List Courses](actions/list-courses.md) | `GET /courses.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/view-all-courses-api) |
| [List Organization Portals](actions/list-organization-portals.md) | `GET {{credentials.academyUrl}}/api/v4/org/portals.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/get-the-organization-id-of-your-account-portal) |
| [List Upcoming Sessions](actions/list-upcoming-sessions.md) | `GET /talks.json` | [docs](https://help.trainercentral.com/portal/en/kb/articles/view-all-upcoming-sessions) |
