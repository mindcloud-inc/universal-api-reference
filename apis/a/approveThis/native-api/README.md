# ApproveThis: Native API Reference

A consolidated summary of ApproveThis's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://app.approvethis.com/docs/api
- **API base URL:** `https://app.approvethis.com/api/v1`

## Authentication

### API Token

Use an ApproveThis API token and workspace ID.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · ApproveThis workspace ID used for template and workflow operations.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.approvethis.com/docs/api)

## API conventions

Responses from this API use JSON. The total page count is read from `meta.lastPage`. The current page number is read from `meta.currentPage`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://app.approvethis.com/docs/api) |
| [Create Workflow](actions/create-workflow.md) | `POST /templates/:template/workflow` | [docs](https://app.approvethis.com/docs/api) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:template` | [docs](https://app.approvethis.com/docs/api) |
| [Generate Template](actions/generate-template.md) | `POST /templates/generate` | [docs](https://app.approvethis.com/docs/api) |
| [Get Template](actions/get-template.md) | `GET /templates/:template` | [docs](https://app.approvethis.com/docs/api) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:workflow` | [docs](https://app.approvethis.com/docs/api) |
| [List Template Fields](actions/list-template-fields.md) | `GET /templates/:template/fields` | [docs](https://app.approvethis.com/docs/api) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://app.approvethis.com/docs/api) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://app.approvethis.com/docs/api) |
| [Update Template](actions/update-template.md) | `PUT /templates/:template` | [docs](https://app.approvethis.com/docs/api) |
