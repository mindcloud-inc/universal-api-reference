# Incontrol: Native API Reference

A consolidated summary of Incontrol's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)
- **OpenAPI specification:** https://portal.incontrol.app/swagger/publicApiV1/swagger.json
- **API base URL:** `https://portal.incontrol.app`

## Authentication

### API Key

Use a service account token created in Organization > Service accounts.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://helpcenter.incontrol.app/en/hoe-koppel-ik-incontrol-middels-een-api)

## Pagination

Use `perPage` in the query string to set the page size (default 50; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderBy` in the query string. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Document](actions/download-document.md) | `GET /api/v1/document/{{id}}/download` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Download File](actions/download-file.md) | `GET /api/v1/file/{{id}}/download` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Case](actions/get-case.md) | `GET /api/v1/case/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Case Note](actions/get-case-note.md) | `GET /api/v1/casenote/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Document](actions/get-document.md) | `GET /api/v1/document/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Draft](actions/get-draft.md) | `GET /api/v1/draft/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get File](actions/get-file.md) | `GET /api/v1/file/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Form](actions/get-form.md) | `GET /api/v1/form/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Notification](actions/get-notification.md) | `GET /api/v1/notification/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Organization](actions/get-organization.md) | `GET /api/v1/organization/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Get User](actions/get-user.md) | `GET /api/v1/user/{{id}}` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Case Notes](actions/list-case-notes.md) | `GET /api/v1/casenote` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Cases](actions/list-cases.md) | `GET /api/v1/case` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Documents](actions/list-documents.md) | `GET /api/v1/document` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Drafts](actions/list-drafts.md) | `GET /api/v1/draft` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Form Templates](actions/list-form-templates.md) | `GET /api/v1/formtemplate` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Forms](actions/list-forms.md) | `GET /api/v1/form` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Local Data Connectors](actions/list-local-data-connectors.md) | `GET /api/v1/localdata` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Notifications](actions/list-notifications.md) | `GET /api/v1/notification` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Organizations](actions/list-organizations.md) | `GET /api/v1/organization` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v1/task` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [List Users](actions/list-users.md) | `GET /api/v1/user` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
| [Verify API Token](actions/verify-api-token.md) | `GET /api/v1/testtoken` | [docs](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)) |
