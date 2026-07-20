# EasyContent: Native API Reference

A consolidated summary of EasyContent's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://easycontent.io/content-api
- **OpenAPI specification:** https://easycontent.io/swagger
- **API base URL:** `https://easycontent.io/api`

## Authentication

### API Key

Bearer token authentication for EasyContent API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://easycontent.io/content-api)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Content Item Assignees And Due Dates](actions/change-content-item-assignees-and-due-dates.md) | `POST /zapier/actions/create/change_item_assignees_and_due_dates` | [docs](https://easycontent.io/content-api) |
| [Change Content Item Status](actions/change-content-item-status.md) | `POST /zapier/actions/create/change_item_status` | [docs](https://easycontent.io/content-api) |
| [Check API Key](actions/check-api-key.md) | `GET /v2/content/auth` | [docs](https://easycontent.io/content-api) |
| [Check Zapier Auth](actions/check-zapier-auth.md) | `GET /zapier/auth` | [docs](https://easycontent.io/content-api) |
| [Create Item](actions/create-item.md) | `POST /zapier/actions/create/create_an_item` | [docs](https://easycontent.io/content-api) |
| [Get Brief](actions/get-brief.md) | `GET /v2/content/briefs/:briefId` | [docs](https://easycontent.io/content-api) |
| [Get Category](actions/get-category.md) | `GET /v2/content/categories/:categoryId` | [docs](https://easycontent.io/content-api) |
| [Get Content Item](actions/get-content-item.md) | `GET /v2/content/content-items/:contentItemId` | [docs](https://easycontent.io/content-api) |
| [Get Template](actions/get-template.md) | `GET /v2/content/templates/:templateId` | [docs](https://easycontent.io/content-api) |
| [List Briefs](actions/list-briefs.md) | `GET /v2/content/briefs` | [docs](https://easycontent.io/content-api) |
| [List Categories](actions/list-categories.md) | `GET /v2/content/categories` | [docs](https://easycontent.io/content-api) |
| [List Content Items](actions/list-content-items.md) | `GET /v2/content/content-items` | [docs](https://easycontent.io/content-api) |
| [List Project Categories](actions/list-project-categories.md) | `GET /zapier/resources/categories` | [docs](https://easycontent.io/content-api) |
| [List Project Content Items](actions/list-project-content-items.md) | `GET /zapier/resources/articles` | [docs](https://easycontent.io/content-api) |
| [List Project Templates](actions/list-project-templates.md) | `GET /zapier/resources/templates` | [docs](https://easycontent.io/content-api) |
| [List Projects](actions/list-projects.md) | `GET /zapier/resources/projects` | [docs](https://easycontent.io/content-api) |
| [List Status Users](actions/list-status-users.md) | `GET /zapier/resources/users-that-can-be-assigned-to-status` | [docs](https://easycontent.io/content-api) |
| [List Template Content Items](actions/list-template-content-items.md) | `GET /v2/content/templates/:templateId/content-items` | [docs](https://easycontent.io/content-api) |
| [List Templates](actions/list-templates.md) | `GET /v2/content/templates` | [docs](https://easycontent.io/content-api) |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | `GET /zapier/resources/statuses` | [docs](https://easycontent.io/content-api) |
