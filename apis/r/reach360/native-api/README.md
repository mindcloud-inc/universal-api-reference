# Reach360: Native API Reference

A consolidated summary of Reach360's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.articulatesupport.com/article/Reach-360-API
- **API base URL:** `https://api.reach360.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.articulatesupport.com/article/Reach-360-Introduction-to-Reach-360-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `users`. The next-page cursor is read from `nextUrl`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Follow the complete next-page URL returned by the API.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | `PUT /groups/:groupId/users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://www.articulatesupport.com/article/Reach-360-Groups-API) |
| [Create Invitation](actions/create-invitation.md) | `POST /invitations` | [docs](https://www.articulatesupport.com/article/Reach-360-Invitations-API) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://www.articulatesupport.com/article/Reach-360-Webhooks-API) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:groupId` | [docs](https://www.articulatesupport.com/article/Reach-360-Groups-API) |
| [Delete Invitation](actions/delete-invitation.md) | `DELETE /invitations/:invitationId` | [docs](https://www.articulatesupport.com/article/Reach-360-Invitations-API) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Users-API) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://www.articulatesupport.com/article/Reach-360-Webhooks-API) |
| [Enroll Group In Course](actions/enroll-group-in-course.md) | `PUT /courses/:courseId/groups/:groupId` | [docs](https://www.articulatesupport.com/article/Reach-360-Course-Enrollments-API) |
| [Enroll Group In Learning Path](actions/enroll-group-in-learning-path.md) | `PUT /learning-paths/:learningPathId/groups/:groupId` | [docs](https://www.articulatesupport.com/article/Reach-360-Learning-Path-Enrollments-API) |
| [Enroll User In Course](actions/enroll-user-in-course.md) | `PUT /courses/:courseId/users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Course-Enrollments-API) |
| [Enroll User In Learning Path](actions/enroll-user-in-learning-path.md) | `PUT /learning-paths/:learningPathId/users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Learning-Path-Enrollments-API) |
| [Get Activity Report](actions/get-activity-report.md) | `GET /reports/activity` | [docs](https://www.articulatesupport.com/article/Reach-360-Reports-API) |
| [Get Course](actions/get-course.md) | `GET /courses/:courseId` | [docs](https://www.articulatesupport.com/article/Reach-360-Courses-API) |
| [Get Course Report](actions/get-course-report.md) | `GET /reports/courses/:courseId` | [docs](https://www.articulatesupport.com/article/Reach-360-Reports-API) |
| [Get Group](actions/get-group.md) | `GET /groups/:groupId` | [docs](https://www.articulatesupport.com/article/Reach-360-Groups-API) |
| [Get Invitation](actions/get-invitation.md) | `GET /invitations/:invitationId` | [docs](https://www.articulatesupport.com/article/Reach-360-Invitations-API) |
| [Get Learner Report](actions/get-learner-report.md) | `GET /reports/learners/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Reports-API) |
| [Get Learning Path](actions/get-learning-path.md) | `GET /learning-paths/:learningPathId` | [docs](https://www.articulatesupport.com/article/Reach-360-Learning-Paths-API) |
| [Get Learning Path Courses Report](actions/get-learning-path-courses-report.md) | `GET /reports/learning-paths/:learningPathId/courses` | [docs](https://www.articulatesupport.com/article/Reach-360-Reports-API) |
| [Get Learning Path Learners Report](actions/get-learning-path-learners-report.md) | `GET /reports/learning-paths/:learningPathId/learners` | [docs](https://www.articulatesupport.com/article/Reach-360-Reports-API) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Users-API) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhookId` | [docs](https://www.articulatesupport.com/article/Reach-360-Webhooks-API) |
| [Import Course Completion](actions/import-course-completion.md) | `POST /courses/:courseId/users/:userId/completions` | [docs](https://www.articulatesupport.com/article/Reach-360-Import-Course-Completion-API) |
| [List Courses](actions/list-courses.md) | `GET /courses` | [docs](https://www.articulatesupport.com/article/Reach-360-Courses-API) |
| [List Group Users](actions/list-group-users.md) | `GET /groups/:groupId/users` | [docs](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://www.articulatesupport.com/article/Reach-360-Groups-API) |
| [List Invitations](actions/list-invitations.md) | `GET /invitations` | [docs](https://www.articulatesupport.com/article/Reach-360-Invitations-API) |
| [List Learning Path Courses](actions/list-learning-path-courses.md) | `GET /learning-paths/:learningPathId/courses` | [docs](https://www.articulatesupport.com/article/Reach-360-Learning-Paths-API) |
| [List Learning Paths](actions/list-learning-paths.md) | `GET /learning-paths` | [docs](https://www.articulatesupport.com/article/Reach-360-Learning-Paths-API) |
| [List User Favorites](actions/list-user-favorites.md) | `GET /users/:userId/favorites` | [docs](https://www.articulatesupport.com/article/Reach-360-Favorites-API) |
| [List User Groups](actions/list-user-groups.md) | `GET /users/:userId/groups` | [docs](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.articulatesupport.com/article/Reach-360-Users-API) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://www.articulatesupport.com/article/Reach-360-Webhooks-API) |
| [Remove User From Group](actions/remove-user-from-group.md) | `DELETE /groups/:groupId/users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API) |
| [Unenroll Group From Course](actions/unenroll-group-from-course.md) | `DELETE /courses/:courseId/groups/:groupId` | [docs](https://www.articulatesupport.com/article/Reach-360-Course-Enrollments-API) |
| [Unenroll Group From Learning Path](actions/unenroll-group-from-learning-path.md) | `DELETE /learning-paths/:learningPathId/groups/:groupId` | [docs](https://www.articulatesupport.com/article/Reach-360-Learning-Path-Enrollments-API) |
| [Unenroll User From Course](actions/unenroll-user-from-course.md) | `DELETE /courses/:courseId/users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Course-Enrollments-API) |
| [Unenroll User From Learning Path](actions/unenroll-user-from-learning-path.md) | `DELETE /learning-paths/:learningPathId/users/:userId` | [docs](https://www.articulatesupport.com/article/Reach-360-Learning-Path-Enrollments-API) |
| [Update Group](actions/update-group.md) | `PUT /groups/:groupId` | [docs](https://www.articulatesupport.com/article/Reach-360-Groups-API) |
