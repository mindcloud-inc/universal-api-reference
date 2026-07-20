# DoneDone: Native API Reference

A consolidated summary of DoneDone's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://donedone.com/help-docs/public-api-webhooks/
- **OpenAPI specification:** https://donedone.com/help-docs/public-api-webhooks/
- **API base URL:** `https://2.donedone.com/public-api`

## Authentication

### Basic Authentication

Connect with your DoneDone login email address and API token.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://donedone.com/help-docs/public-api-webhooks/)

## API conventions

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Task Comment](actions/add-task-comment.md) | `POST /:account_id/internal-projects/:internal_project_id/tasks/:task_id/comment-only` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Create Task](actions/create-task.md) | `POST /:account_id/internal-projects/:internal_project_id/tasks` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Delete Task](actions/delete-task.md) | `DELETE /:account_id/internal-projects/:internal_project_id/tasks/:task_id` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Get Profile](actions/get-profile.md) | `GET /:account_id/profile` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Get Project](actions/get-project.md) | `GET /:account_id/internal-projects/:internal_project_id` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Get Task](actions/get-task.md) | `GET /:account_id/internal-projects/:internal_project_id/tasks/:task_id` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Get Task History](actions/get-task-history.md) | `GET /:account_id/internal-projects/:internal_project_id/tasks/:task_id/history` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Get Workflow](actions/get-workflow.md) | `GET /:account_id/workflows/:workflow_id` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [List Project Priorities](actions/list-project-priorities.md) | `GET /:account_id/internal-projects/:internal_project_id/priorities` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [List Project Statuses](actions/list-project-statuses.md) | `GET /:account_id/internal-projects/:internal_project_id/statuses` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [List Project Tags](actions/list-project-tags.md) | `GET /:account_id/internal-projects/:internal_project_id/tags` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [List Projects](actions/list-projects.md) | `GET /:account_id/internal-projects/for-selection` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | `GET /:account_id/workflows/:workflow_id/statuses` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [List Workflows](actions/list-workflows.md) | `GET /:account_id/workflows/for-selection` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Update Task Priority](actions/update-task-priority.md) | `PUT /:account_id/internal-projects/:internal_project_id/tasks/:task_id/priority` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Update Task Status](actions/update-task-status.md) | `PUT /:account_id/internal-projects/:internal_project_id/tasks/:task_id/status` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
| [Update Task Title](actions/update-task-title.md) | `PUT /:account_id/internal-projects/:internal_project_id/tasks/:task_id/title` | [docs](https://donedone.com/help-docs/public-api-webhooks/) |
