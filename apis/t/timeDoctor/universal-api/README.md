# <img src="https://images.mindcloud.co/apps/icons/time-doctor_1776292247666.png" alt="Time Doctor logo" width="28" height="28"> Time Doctor: Universal API

Time Doctor is a workforce analytics and time tracking platform for teams. This app wraps the Time Doctor API for company, user, project, folder, task, and work-tracking operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timeDoctor/latest
- **Category:** Human Resources / HRIS
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.timedoctor.com
- **Vendor API docs:** https://api2.timedoctor.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authorization](actions/get-authorization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [List User Tokens](actions/list-user-tokens.md) | GET | Retrieves user tokens from Time Doctor. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Unrated Categories Count](actions/get-unrated-categories-count.md) | GET | Retrieves unrated category counts from Time Doctor. |
| [List User Categories](actions/get-user-categories.md) | GET | Retrieves user categories from Time Doctor. |
| [List Categories](actions/list-categories.md) | GET | Retrieves productivity categories from Time Doctor. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Time Doctor. |
| [Get Company Timezones](actions/get-company-timezones.md) | GET | Retrieves company timezones from Time Doctor. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Time Doctor. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Get Invitation Status](actions/get-invitation-status.md) | GET | Retrieves invitation status from Time Doctor. |
| [Invite User](actions/invite-user.md) | POST | Creates a new user invitation in Time Doctor. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Time Doctor. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Time Doctor. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Time Doctor. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Time Doctor. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Time Doctor. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Leave Stats](actions/get-leave-stats.md) | GET | Retrieves leave stats from Time Doctor. |
| [List Work Schedule Issues](actions/list-work-schedule-issues.md) | GET | Retrieves work schedule issues from Time Doctor. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Work Schedules](actions/list-work-schedules.md) | GET | Retrieves work schedules from Time Doctor. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Time Doctor. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Time Doctor. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Time Doctor. |
| [Delete Task](actions/delete-task.md) | DELETE | Archives or restores a task in Time Doctor. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Time Doctor. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Time Doctor. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Time Doctor. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Authorization](actions/get-authorization.md) | GET | Retrieves authorization details from Time Doctor. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Time Doctor. |
| [Get User Totals](actions/get-user-totals.md) | GET | Retrieves user totals from Time Doctor. |
| [List Managed Users](actions/list-managed-users.md) | GET | Retrieves managed users from Time Doctor. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Time Doctor. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Time Doctor. |

