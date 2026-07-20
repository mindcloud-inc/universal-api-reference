# <img src="https://images.mindcloud.co/apps/icons/images-21_1776200222450.png" alt="Onethread logo" width="28" height="28"> Onethread: Universal API

Project management and collaboration wrapper for Onethread.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onethread/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.onethread.app/
- **Vendor API docs:** https://docs.onethreadapp.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Meta Data](actions/get-user-meta-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-user-meta-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Timeline](actions/get-account-timeline.md) | GET |  |
| [Get Company Activity Log](actions/get-company-activity-log.md) | GET |  |
| [Get Company Tracking](actions/get-company-tracking.md) | GET |  |
| [Get Track](actions/get-track.md) | POST |  |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Profile](actions/get-company-profile.md) | GET |  |
| [Get Company Role](actions/get-company-role.md) | GET |  |
| [Search Companies](actions/search-companies.md) | GET |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Room Chats](actions/list-room-chats.md) | GET |  |
| [List Rooms](actions/list-rooms.md) | GET |  |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Suggest Labels](actions/suggest-labels.md) | GET |  |
| [Suggest Labels By Company](actions/suggest-labels-by-company.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | POST |  |
| [List Unread Messages](actions/list-unread-messages.md) | GET |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Get Notifications](actions/get-notifications.md) | GET |  |
| [Mark Notifications Seen](actions/mark-notifications-seen.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project List Overview](actions/get-project-list-overview.md) | GET |  |
| [Get Project Overview](actions/get-project-overview.md) | GET |  |
| [Get Project Tracking](actions/get-project-tracking.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Show Project Files](actions/show-project-files.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Subtask Tracking](actions/get-subtask-tracking.md) | GET |  |
| [Get Task Tracking](actions/get-task-tracking.md) | GET |  |
| [List Project Tasks](actions/list-project-tasks.md) | GET |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Associate Members](actions/list-associate-members.md) | GET |  |
| [List Team Members](actions/list-team-members.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Meta Data](actions/get-user-meta-data.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |
| [Get Account Skill Area](actions/get-account-skill-area.md) | GET |  |
| [Get Auth Token (Email and Password)](actions/get-auth-token-email-and-password.md) | POST |  |

