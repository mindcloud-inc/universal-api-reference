# <img src="https://images.mindcloud.co/apps/icons/icon-256x256_1773414148374.png" alt="TalentLMS logo" width="28" height="28"> TalentLMS: Universal API

TalentLMS: Manage users, courses, groups, branches, and enrollments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/talentLMS/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.talentlms.com
- **Vendor API docs:** https://documenter.getpostman.com/view/31867199/2sAY548Kou

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Create Branch](actions/create-branch.md) | POST | Creates a new branch in TalentLMS. |
| [Delete Branch](actions/delete-branch.md) | DELETE | Deletes an existing branch from TalentLMS. |
| [Get Branch](actions/get-branch.md) | GET | Retrieves a branch from a TalentLMS domain. |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from a TalentLMS domain. |

### Branchcourse

| Action | Method | Description |
| --- | --- | --- |
| [Add Course to Branch](actions/add-course-to-branch.md) | POST | Adds a course to a branch in TalentLMS. |
| [Remove Course from Branch](actions/remove-course-from-branch.md) | DELETE | Removes a course from a branch in TalentLMS. |

### Branchuser

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Branch](actions/add-user-to-branch.md) | POST | Adds a user to a branch in TalentLMS. |
| [Remove User from Branch](actions/remove-user-from-branch.md) | DELETE | Removes a user from a branch in TalentLMS. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Create Course](actions/create-course.md) | POST | Creates a new course in TalentLMS. |
| [Delete Course](actions/delete-course.md) | DELETE | Deletes an existing course from TalentLMS. |
| [Get Course](actions/get-course.md) | GET | Retrieves a course from a TalentLMS domain. |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from a TalentLMS domain. |

### Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Enroll User to Course](actions/enroll-user-to-course.md) | POST | Enrolls a user in a course in TalentLMS. |
| [Remove User from Course](actions/remove-user-from-course.md) | DELETE | Removes a user from a course in TalentLMS. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in TalentLMS. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from TalentLMS. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from a TalentLMS domain. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from a TalentLMS domain. |

### Groupmembership

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Group](actions/add-user-to-group.md) | POST | Adds a user to a group in TalentLMS. |
| [Remove User from Group](actions/remove-user-from-group.md) | DELETE | Removes a user from a group in TalentLMS. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in TalentLMS. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from TalentLMS. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from a TalentLMS domain. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a TalentLMS domain. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in TalentLMS. |

