# Uspacy: Native API Reference

A consolidated summary of Uspacy's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://uspacy.readme.io/reference/introduction
- **API base URL:** `https://{site}`

## Authentication

### Workspace JWT

Use your workspace site and a bearer token minted from Uspacy sign-in.

### Credentials

- **Workspace Site:** `site` · required · Your full Uspacy workspace host, for example acme.uspacy.com.
- **JWT Token:** `jwt` · required · Bearer JWT access token returned by the documented Uspacy sign-in flow.
- **Refresh Token:** `refreshToken` · optional · Refresh token returned by Uspacy sign-in; store it for later manual refresh.

Send these headers with each API request:

```http
Authorization: Bearer <jwt>
```

[Official authentication documentation](https://uspacy.readme.io/reference/post_auth-v1-auth-sign-in-1)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /activities/v1/activities` | [docs](https://uspacy.readme.io/reference/post_activities-v1-activities) |
| [Create Comment](actions/create-comment.md) | `POST /comments/v1/comments` | [docs](https://uspacy.readme.io/reference/commentscontroller_createcomment) |
| [Create CRM Entity Item](actions/create-crm-entity-item.md) | `POST /crm/v1/entities/:entity` | [docs](https://uspacy.readme.io/reference/post_crm-v1-entities-entity) |
| [Create Outgoing Webhook](actions/create-outgoing-webhook.md) | `POST /company/v1/webhooks` | [docs](https://uspacy.readme.io/reference/post_company-v1-webhooks) |
| [Create Task](actions/create-task.md) | `POST /tasks/v1/tasks` | [docs](https://uspacy.readme.io/reference/post_tasks-v1-tasks-1) |
| [Get CRM Entity Item](actions/get-crm-entity-item.md) | `GET /crm/v1/entities/:entity/:itemId` | [docs](https://uspacy.readme.io/reference/get_crm-v1-entities-entity-itemid) |
| [Get Self Profile](actions/get-self-profile.md) | `GET /company/v1/users/me` | [docs](https://uspacy.readme.io/reference/get_company-v1-users-me-1) |
| [Get Task](actions/get-task.md) | `GET /tasks/v1/tasks/:taskId` | [docs](https://uspacy.readme.io/reference/get_tasks-v1-tasks-taskid-1) |
| [List Activities](actions/list-activities.md) | `GET /activities/v1/activities` | [docs](https://uspacy.readme.io/reference/get_activities-v1-activities) |
| [List Comments](actions/list-comments.md) | `GET /comments/v1/comments` | [docs](https://uspacy.readme.io/reference/commentscontroller_getcomments) |
| [List Companies](actions/list-companies.md) | `GET /crm/v1/entities/companies` | [docs](https://uspacy.readme.io/reference/get_crm-v1-entities-companies) |
| [List Contacts](actions/list-contacts.md) | `GET /crm/v1/entities/contacts` | [docs](https://uspacy.readme.io/reference/get_crm-v1-entities-contacts) |
| [List CRM Entities](actions/list-crm-entities.md) | `GET /crm/v1/entity` | [docs](https://uspacy.readme.io/reference/get_crm-v1-entity) |
| [List CRM Entity Items](actions/list-crm-entity-items.md) | `GET /crm/v1/entities/:entity` | [docs](https://uspacy.readme.io/reference/get_crm-v1-entities-entity) |
| [List Deals](actions/list-deals.md) | `GET /crm/v1/entities/deals` | [docs](https://uspacy.readme.io/reference/get_crm-v1-entities-deals) |
| [List Outgoing Webhooks](actions/list-outgoing-webhooks.md) | `GET /company/v1/webhooks` | [docs](https://uspacy.readme.io/reference/get_company-v1-webhooks) |
| [List Task Stages](actions/list-task-stages.md) | `GET /tasks/v1/stages` | [docs](https://uspacy.readme.io/reference/get_tasks-v1-stages-1) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks/v1/tasks` | [docs](https://uspacy.readme.io/reference/get_tasks-v1-tasks-1) |
| [List Users](actions/list-users.md) | `GET /company/v1/users` | [docs](https://uspacy.readme.io/reference/get_company-v1-users-1) |
| [Move Task To Stage](actions/move-task-to-stage.md) | `POST /tasks/v1/stages/:stageId/moveTask` | [docs](https://uspacy.readme.io/reference/post_tasks-v1-stages-stageid-movetask-1) |
| [Search Workspace Data](actions/search-workspace-data.md) | `GET /search/v1/search` | [docs](https://uspacy.readme.io/reference/get_search-v1-search-1) |
| [Toggle Outgoing Webhook Status](actions/toggle-outgoing-webhook-status.md) | `PATCH /company/v1/webhooks/:webhookId/toggle` | [docs](https://uspacy.readme.io/reference/patch_company-v1-webhooks-webhookid-toggle) |
| [Update CRM Entity Item](actions/update-crm-entity-item.md) | `PATCH /crm/v1/entities/:entity/:itemId` | [docs](https://uspacy.readme.io/reference/patch_crm-v1-entities-entity-itemid) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/v1/tasks/:taskId` | [docs](https://uspacy.readme.io/reference/patch_tasks-v1-tasks-taskid-1) |
