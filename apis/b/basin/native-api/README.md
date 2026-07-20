# Basin: Native API Reference

A consolidated summary of Basin's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://usebasin.com/api_docs/index.html
- **OpenAPI specification:** https://usebasin.com/api_docs/v1/swagger.yaml
- **API base URL:** `https://usebasin.com`

## Authentication

### API Key - Custom

### Credentials

- **API Key:** `apiKey` · required

[Official authentication documentation](https://docs.usebasin.com/developer-features/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `meta.page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST /api/v1/forms/` | [docs](https://usebasin.com/api_docs/index.html) |
| [Create Project](actions/create-project.md) | `POST /api/v1/projects/` | [docs](https://usebasin.com/api_docs/index.html) |
| [Delete Form](actions/delete-form.md) | `DELETE /api/v1/forms/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v1/projects/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /api/v1/submissions/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [List Domains](actions/list-domains.md) | `GET /api/v1/domains` | [docs](https://usebasin.com/api_docs/index.html) |
| [List Form Views](actions/list-form-views.md) | `GET /api/v1/form_views` | [docs](https://usebasin.com/api_docs/index.html) |
| [List Forms](actions/list-forms.md) | `GET /api/v1/forms` | [docs](https://usebasin.com/api_docs/index.html) |
| [List Projects](actions/list-projects.md) | `GET /api/v1/projects` | [docs](https://usebasin.com/api_docs/index.html) |
| [List Submissions](actions/list-submissions.md) | `GET /api/v1/submissions` | [docs](https://usebasin.com/api_docs/index.html) |
| [Refire Submission Webhooks](actions/refire-submission-webhooks.md) | `POST /api/v1/submissions/:id/refire_webhooks` | [docs](https://usebasin.com/api_docs/index.html) |
| [Refire Submission Webhooks Batch](actions/refire-submission-webhooks-batch.md) | `POST /api/v1/submissions/refire_webhooks` | [docs](https://usebasin.com/api_docs/index.html) |
| [Show Form](actions/show-form.md) | `GET /api/v1/forms/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Show Form View](actions/show-form-view.md) | `GET /api/v1/form_views/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Show Project](actions/show-project.md) | `GET /api/v1/projects/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Show Submission](actions/show-submission.md) | `GET /api/v1/submissions/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Update Form](actions/update-form.md) | `PUT /api/v1/forms/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Update Project](actions/update-project.md) | `PUT /api/v1/projects/:id` | [docs](https://usebasin.com/api_docs/index.html) |
| [Update Submission](actions/update-submission.md) | `PATCH /api/v1/submissions/:id` | [docs](https://usebasin.com/api_docs/index.html) |
