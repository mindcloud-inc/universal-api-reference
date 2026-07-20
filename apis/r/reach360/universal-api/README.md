# <img src="https://images.mindcloud.co/apps/icons/reach360_1773945594766.png" alt="Reach360 logo" width="28" height="28"> Reach360: Universal API

Manage Reach360 learners, groups, enrollments, and reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reach360/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.articulate.com/360/reach
- **Vendor API docs:** https://www.articulatesupport.com/article/Reach-360-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List User Favorites](actions/list-user-favorites.md) | GET | Retrieves a user's favorite items from Reach360. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Learning Path](actions/get-learning-path.md) | GET | Retrieves a learning path from Reach360 by ID. |
| [List Learning Paths](actions/list-learning-paths.md) | GET | Retrieves all learning paths from Reach360. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Reach360. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Reach360 by ID. |
| [List Groups](actions/list-groups.md) | GET | Retrieves all groups from Reach360. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Reach360. |
| [List User Groups](actions/list-user-groups.md) | GET | Retrieves all groups for a Reach360 user. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Reach360. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Create Invitation](actions/create-invitation.md) | POST | Creates a new invitation in Reach360. |
| [Delete Invitation](actions/delete-invitation.md) | DELETE | Deletes an existing invitation from Reach360. |
| [Get Invitation](actions/get-invitation.md) | GET | Retrieves an invitation from Reach360 by ID. |
| [List Invitations](actions/list-invitations.md) | GET | Retrieves all invitations from Reach360. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Course](actions/get-course.md) | GET | Retrieves a course from Reach360 by ID. |
| [List Courses](actions/list-courses.md) | GET | Retrieves all courses from Reach360. |
| [List Learning Path Courses](actions/list-learning-path-courses.md) | GET | Retrieves all courses in a Reach360 learning path. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | POST | Adds a user to a Reach360 group. |
| [Enroll Group In Course](actions/enroll-group-in-course.md) | POST | Enrolls a group in a Reach360 course. |
| [Enroll Group In Learning Path](actions/enroll-group-in-learning-path.md) | POST | Enrolls a group in a Reach360 learning path. |
| [Enroll User In Course](actions/enroll-user-in-course.md) | POST | Enrolls a user in a Reach360 course. |
| [Enroll User In Learning Path](actions/enroll-user-in-learning-path.md) | POST | Enrolls a user in a Reach360 learning path. |
| [Import Course Completion](actions/import-course-completion.md) | POST | Imports a user's course completion into Reach360. |
| [Remove User From Group](actions/remove-user-from-group.md) | DELETE | Removes a user from a Reach360 group. |
| [Unenroll Group From Course](actions/unenroll-group-from-course.md) | DELETE | Removes a group from a Reach360 course. |
| [Unenroll Group From Learning Path](actions/unenroll-group-from-learning-path.md) | DELETE | Removes a group from a Reach360 learning path. |
| [Unenroll User From Course](actions/unenroll-user-from-course.md) | DELETE | Removes a user from a Reach360 course. |
| [Unenroll User From Learning Path](actions/unenroll-user-from-learning-path.md) | DELETE | Removes a user from a Reach360 learning path. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Report](actions/get-activity-report.md) | GET | Retrieves the activity report from Reach360. |
| [Get Course Report](actions/get-course-report.md) | GET | Retrieves a course report from Reach360. |
| [Get Learner Report](actions/get-learner-report.md) | GET | Retrieves a learner report from Reach360 by user. |
| [Get Learning Path Courses Report](actions/get-learning-path-courses-report.md) | GET | Retrieves a learning path courses report from Reach360. |
| [Get Learning Path Learners Report](actions/get-learning-path-learners-report.md) | GET | Retrieves a learning path learners report from Reach360. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves all users from Reach360. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Reach360. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Reach360 by ID. |
| [List Group Users](actions/list-group-users.md) | GET | Retrieves all users in a Reach360 group. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Reach360. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Reach360. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Reach360 by ID. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhooks from Reach360. |

