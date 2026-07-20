# Onethread: Native API Reference

A consolidated summary of Onethread's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.onethreadapp.com/
- **OpenAPI specification:** https://api.onethread.app/
- **API base URL:** `https://api.onethread.app/api/v1`

## Authentication

### Email and Password

Login with an Onethread account email and password.

### Credentials

- **Email:** `username` · required
- **Password:** `password` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://docs.onethreadapp.com/3.-getting-started/3.2-log-in)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /accounts/` | [docs](https://api.onethread.app/) |
| [Get Account Skill Area](actions/get-account-skill-area.md) | `GET /accounts/skill-area` | [docs](https://api.onethread.app/) |
| [Get Account Timeline](actions/get-account-timeline.md) | `GET /accounts/timeline` | [docs](https://api.onethread.app/) |
| [Get Auth Token (Email and Password)](actions/get-auth-token-email-and-password.md) | `POST /accounts/login` | [docs](https://docs.onethreadapp.com/3.-getting-started/3.2-log-in) |
| [Get Company Activity Log](actions/get-company-activity-log.md) | `GET /company/activity-log` | [docs](https://api.onethread.app/) |
| [Get Company Profile](actions/get-company-profile.md) | `GET /company/individual` | [docs](https://api.onethread.app/) |
| [Get Company Role](actions/get-company-role.md) | `GET /company/user-role-company` | [docs](https://api.onethread.app/) |
| [Get Company Tracking](actions/get-company-tracking.md) | `GET /track/company` | [docs](https://api.onethread.app/) |
| [Get Notifications](actions/get-notifications.md) | `GET /notifications/get` | [docs](https://api.onethread.app/) |
| [Get Project List Overview](actions/get-project-list-overview.md) | `GET /projects/list/overview` | [docs](https://api.onethread.app/) |
| [Get Project Overview](actions/get-project-overview.md) | `GET /projects/overview` | [docs](https://api.onethread.app/) |
| [Get Project Tracking](actions/get-project-tracking.md) | `GET /track/project` | [docs](https://api.onethread.app/) |
| [Get Subtask Tracking](actions/get-subtask-tracking.md) | `GET /track/subtask` | [docs](https://api.onethread.app/) |
| [Get Task Tracking](actions/get-task-tracking.md) | `GET /track/task` | [docs](https://api.onethread.app/) |
| [Get Track](actions/get-track.md) | `POST /track` | [docs](https://api.onethread.app/) |
| [Get User Meta Data](actions/get-user-meta-data.md) | `GET /accounts/user-meta-data` | [docs](https://api.onethread.app/) |
| [List Associate Members](actions/list-associate-members.md) | `GET /teams/associate-list` | [docs](https://api.onethread.app/) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://api.onethread.app/) |
| [List Messages](actions/list-messages.md) | `POST /messages` | [docs](https://api.onethread.app/) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /projects/tasks` | [docs](https://api.onethread.app/) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.onethread.app/) |
| [List Room Chats](actions/list-room-chats.md) | `GET /rooms/chats` | [docs](https://api.onethread.app/) |
| [List Rooms](actions/list-rooms.md) | `GET /rooms/list` | [docs](https://api.onethread.app/) |
| [List Team Members](actions/list-team-members.md) | `GET /teams/member-list` | [docs](https://api.onethread.app/) |
| [List Unread Messages](actions/list-unread-messages.md) | `GET /messages/unread-messages` | [docs](https://api.onethread.app/) |
| [Mark Notifications Seen](actions/mark-notifications-seen.md) | `GET /notifications/seen` | [docs](https://api.onethread.app/) |
| [Search Companies](actions/search-companies.md) | `GET /company/search` | [docs](https://api.onethread.app/) |
| [Show Project Files](actions/show-project-files.md) | `GET /projects/show-files` | [docs](https://api.onethread.app/) |
| [Suggest Labels](actions/suggest-labels.md) | `GET /labels/suggest` | [docs](https://api.onethread.app/) |
| [Suggest Labels By Company](actions/suggest-labels-by-company.md) | `GET /labels/suggest-by-company` | [docs](https://api.onethread.app/) |
