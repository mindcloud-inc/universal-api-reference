# FlexiFunnels: Native API Reference

A consolidated summary of FlexiFunnels's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://bridge.flexifunnels.com/docs
- **API base URL:** `https://bridge.flexifunnels.com`

## Authentication

### Membership Login

Custom member-login bootstrap for the FlexiFunnels Membership API.

### Credentials

- **Funnel ID:** `funnelId` · required · Numeric membership funnel identifier required by POST /api/login.
- **Device Name:** `deviceName` · optional · Optional device name sent during login.
- **Email:** `email` · required · Membership API login email for the target funnel.

[Official authentication documentation](https://bridge.flexifunnels.com/docs#auth-user-endpoints-POSTapi-login)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /api/login` | [docs](https://bridge.flexifunnels.com/docs#auth-user-endpoints-POSTapi-login) |
| [Course Complete Percentage](actions/course-complete-percentage.md) | `POST /api/completeperc` | [docs](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-completeperc) |
| [Get Courses](actions/get-courses.md) | `POST /api/courselist` | [docs](https://bridge.flexifunnels.com/docs#course-endpoints-POSTapi-courselist) |
| [Get Custom Script](actions/get-custom-script.md) | `POST /api/customscript` | [docs](https://bridge.flexifunnels.com/docs#auth-user-endpoints-POSTapi-customscript) |
| [Get Footer](actions/get-footer.md) | `POST /api/get-footer` | [docs](https://bridge.flexifunnels.com/docs#auth-user-endpoints-POSTapi-get-footer) |
| [Get Gamify Points](actions/get-gamify-points.md) | `POST /api/get-gamify-points` | [docs](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-get-gamify-points) |
| [Get Goals](actions/get-goals.md) | `POST /api/goallist` | [docs](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-goallist) |
| [Get Lesson Details](actions/get-lesson-details.md) | `POST /api/lesson-details` | [docs](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-lesson-details) |
| [Get Lesson Notes](actions/get-lesson-notes.md) | `POST /api/get-lesson-notes` | [docs](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-get-lesson-notes) |
| [Get Lessons](actions/get-lessons.md) | `POST /api/lessonlist` | [docs](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-lessonlist) |
| [Get Member Points](actions/get-member-points.md) | `POST /api/get-member-points` | [docs](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-get-member-points) |
| [Get Next Badge](actions/get-next-badge.md) | `POST /api/get-next-badge` | [docs](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-get-next-badge) |
| [Get Profile](actions/get-profile.md) | `POST /api/profile` | [docs](https://bridge.flexifunnels.com/docs#auth-user-endpoints-POSTapi-profile) |
| [Get Quiz List](actions/get-quiz-list.md) | `POST /api/quiz-list` | [docs](https://bridge.flexifunnels.com/docs#quiz-endpoints-POSTapi-quiz-list) |
| [Mark Complete](actions/mark-complete.md) | `POST /api/markecomplete` | [docs](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-markecomplete) |
| [Member Badge List](actions/member-badge-list.md) | `POST /api/member-badge-list` | [docs](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-member-badge-list) |
| [Member Reward List](actions/member-reward-list.md) | `POST /api/member-reward-list` | [docs](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-member-reward-list) |
| [Resource List](actions/resource-list.md) | `POST /api/downloadcontent` | [docs](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-downloadcontent) |
| [Search Courses](actions/search-courses.md) | `POST /api/searchcourselist` | [docs](https://bridge.flexifunnels.com/docs#course-endpoints-POSTapi-searchcourselist) |
| [Unlock Mark Complete](actions/unlock-mark-complete.md) | `POST /api/delete-markecomplete` | [docs](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-delete-markecomplete) |
