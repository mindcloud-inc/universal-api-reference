# Worksection: Native API Reference

A consolidated summary of Worksection's API configuration and 55 documented operations, with links to official documentation.

- **Official docs:** https://worksection.com/en/faq/api-start.html
- **API base URL:** `https://min7657.worksection.com/api/admin/v2`

## Authentication

### Administrative API Key

Use a Worksection administrative API key to authorize admin-token requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://worksection.com/en/faq/api-start.html#q1911)

## API conventions

Response data is read from `data`.

## Endpoints (55 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Project](actions/activate-project.md) | `POST /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Add Project Members](actions/add-project-members.md) | `POST /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Close Project](actions/close-project.md) | `POST /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Complete Task](actions/complete-task.md) | `POST /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [Create Comment](actions/create-comment.md) | `POST /` | [docs](https://worksection.com/en/faq/api-comments.html) |
| [Create Contact](actions/create-contact.md) | `POST /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [Create Contact Group](actions/create-contact-group.md) | `POST /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [Create Cost](actions/create-cost.md) | `POST /` | [docs](https://worksection.com/en/faq/api-costs.html) |
| [Create Project](actions/create-project.md) | `POST /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Create Project Group](actions/create-project-group.md) | `POST /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Create Project Tag](actions/create-project-tag.md) | `POST /` | [docs](https://worksection.com/faq/api-tags.html) |
| [Create Project Tag Group](actions/create-project-tag-group.md) | `POST /` | [docs](https://worksection.com/faq/api-tags.html) |
| [Create Task](actions/create-task.md) | `POST /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [Create Task Tag](actions/create-task-tag.md) | `POST /` | [docs](https://worksection.com/faq/api-tags.html) |
| [Create Task Tag Group](actions/create-task-tag-group.md) | `POST /` | [docs](https://worksection.com/faq/api-tags.html) |
| [Create User](actions/create-user.md) | `POST /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [Create User Group](actions/create-user-group.md) | `POST /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [Create Webhook](actions/create-webhook.md) | `POST /` | [docs](https://worksection.com/en/blog/webhooks.html) |
| [Delete Cost](actions/delete-cost.md) | `POST /` | [docs](https://worksection.com/en/faq/api-costs.html) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /` | [docs](https://worksection.com/en/blog/webhooks.html) |
| [Download File](actions/download-file.md) | `GET /` | [docs](https://worksection.com/en/faq/api-files.html) |
| [Get Costs Total](actions/get-costs-total.md) | `GET /` | [docs](https://worksection.com/en/faq/api-costs.html) |
| [Get Project](actions/get-project.md) | `GET /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Get Task](actions/get-task.md) | `GET /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [Get User Schedules](actions/get-user-schedules.md) | `GET /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [List All Tasks](actions/list-all-tasks.md) | `GET /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [List Comments](actions/list-comments.md) | `GET /` | [docs](https://worksection.com/en/faq/api-comments.html) |
| [List Contact Groups](actions/list-contact-groups.md) | `GET /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [List Contacts](actions/list-contacts.md) | `GET /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [List Costs](actions/list-costs.md) | `GET /` | [docs](https://worksection.com/en/faq/api-costs.html) |
| [List Files](actions/list-files.md) | `GET /` | [docs](https://worksection.com/en/faq/api-files.html) |
| [List Project Events](actions/list-project-events.md) | `GET /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [List Project Groups](actions/list-project-groups.md) | `GET /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [List Project Tag Groups](actions/list-project-tag-groups.md) | `GET /` | [docs](https://worksection.com/faq/api-tags.html) |
| [List Project Tags](actions/list-project-tags.md) | `GET /` | [docs](https://worksection.com/faq/api-tags.html) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [List Projects](actions/list-projects.md) | `GET /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [List Task Tag Groups](actions/list-task-tag-groups.md) | `GET /` | [docs](https://worksection.com/faq/api-tags.html) |
| [List Task Tags](actions/list-task-tags.md) | `GET /` | [docs](https://worksection.com/faq/api-tags.html) |
| [List Timers](actions/list-timers.md) | `GET /` | [docs](https://worksection.com/faq/api-timers.html) |
| [List User Groups](actions/list-user-groups.md) | `GET /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [List Users](actions/list-users.md) | `GET /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [List Webhooks](actions/list-webhooks.md) | `GET /` | [docs](https://worksection.com/en/blog/webhooks.html) |
| [Remove Project Members](actions/remove-project-members.md) | `POST /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Reopen Task](actions/reopen-task.md) | `POST /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [Search Tasks](actions/search-tasks.md) | `GET /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [Stop Timer](actions/stop-timer.md) | `POST /` | [docs](https://worksection.com/faq/api-timers.html) |
| [Subscribe](actions/subscribe.md) | `POST /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [Unsubscribe](actions/unsubscribe.md) | `POST /` | [docs](https://worksection.com/en/faq/api-user.html) |
| [Update Cost](actions/update-cost.md) | `POST /` | [docs](https://worksection.com/en/faq/api-costs.html) |
| [Update Project](actions/update-project.md) | `POST /` | [docs](https://worksection.com/en/faq/api-projects.html) |
| [Update Project Tag](actions/update-project-tag.md) | `POST /` | [docs](https://worksection.com/faq/api-tags.html) |
| [Update Task](actions/update-task.md) | `POST /` | [docs](https://worksection.com/en/faq/api-task.html) |
| [Update Task Tag](actions/update-task-tag.md) | `POST /` | [docs](https://worksection.com/faq/api-tags.html) |
| [Update User Schedule](actions/update-user-schedule.md) | `POST /` | [docs](https://worksection.com/en/faq/api-user.html) |
