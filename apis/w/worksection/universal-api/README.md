# <img src="https://images.mindcloud.co/apps/icons/images-3_1775756578076.png" alt="Worksection logo" width="28" height="28"> Worksection: Universal API

Manage Worksection projects, tasks, comments, files, and time tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/worksection/latest
- **Category:** Productivity / Project Management
- **Actions:** 55
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://worksection.com
- **Vendor API docs:** https://worksection.com/en/faq/api-start.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksection/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (55)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [List Comments](actions/list-comments.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Contact Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Group](actions/create-contact-group.md) | POST |  |
| [List Contact Groups](actions/list-contact-groups.md) | GET |  |

### Cost

| Action | Method | Description |
| --- | --- | --- |
| [Create Cost](actions/create-cost.md) | POST |  |
| [Delete Cost](actions/delete-cost.md) | DELETE |  |
| [Get Costs Total](actions/get-costs-total.md) | GET |  |
| [List Costs](actions/list-costs.md) | GET |  |
| [Update Cost](actions/update-cost.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET |  |
| [List Files](actions/list-files.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Activate Project](actions/activate-project.md) | PUT |  |
| [Close Project](actions/close-project.md) | PUT |  |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Project Event

| Action | Method | Description |
| --- | --- | --- |
| [List Project Events](actions/list-project-events.md) | GET |  |

### Project Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Group](actions/create-project-group.md) | POST |  |
| [List Project Groups](actions/list-project-groups.md) | GET |  |

### Project Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Members](actions/add-project-members.md) | POST |  |
| [Remove Project Members](actions/remove-project-members.md) | DELETE |  |

### Project Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Tag](actions/create-project-tag.md) | POST |  |
| [List Project Tags](actions/list-project-tags.md) | GET |  |
| [Update Project Tag](actions/update-project-tag.md) | PUT |  |

### Project Tag Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Tag Group](actions/create-project-tag-group.md) | POST |  |
| [List Project Tag Groups](actions/list-project-tag-groups.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe](actions/subscribe.md) | POST |  |
| [Unsubscribe](actions/unsubscribe.md) | DELETE |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | PUT |  |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List All Tasks](actions/list-all-tasks.md) | GET |  |
| [List Project Tasks](actions/list-project-tasks.md) | GET |  |
| [Reopen Task](actions/reopen-task.md) | PUT |  |
| [Search Tasks](actions/search-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Task Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Tag](actions/create-task-tag.md) | POST |  |
| [List Task Tags](actions/list-task-tags.md) | GET |  |
| [Update Task Tag](actions/update-task-tag.md) | PUT |  |

### Task Tag Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Tag Group](actions/create-task-tag-group.md) | POST |  |
| [List Task Tag Groups](actions/list-task-tag-groups.md) | GET |  |

### Timer

| Action | Method | Description |
| --- | --- | --- |
| [List Timers](actions/list-timers.md) | GET |  |
| [Stop Timer](actions/stop-timer.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [List Users](actions/list-users.md) | GET |  |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Create User Group](actions/create-user-group.md) | POST |  |
| [List User Groups](actions/list-user-groups.md) | GET |  |

### User Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get User Schedules](actions/get-user-schedules.md) | GET |  |
| [Update User Schedule](actions/update-user-schedule.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

