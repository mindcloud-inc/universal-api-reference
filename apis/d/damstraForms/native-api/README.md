# Damstra Forms: Native API Reference

A consolidated summary of Damstra Forms's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://sammapi.docs.apiary.io/#
- **API base URL:** `{baseUrl}`

## Authentication

### API Key

Authenticate Damstra Forms requests with the API key from Organisation Settings.

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · Damstra Forms API root for the account, including /public_api/v2. Example: https://yourcompany.au.damstraforms.com/public_api/v2.

Send these headers with each API request:

```http
Authorization: Token token="<apiKey>"
```

[Official authentication documentation](https://sammapi.docs.apiary.io/#introduction/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `after` in the query string as the pagination cursor; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Form](actions/close-form.md) | `PATCH /forms/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/forms/form-instance/close-a-form) |
| [Create Draft Action](actions/create-draft-action.md) | `POST /actions` | [docs](https://sammapi.docs.apiary.io/#reference/actions/action-collection/create-a-draft-action) |
| [Create Draft Form](actions/create-draft-form.md) | `POST /forms` | [docs](https://sammapi.docs.apiary.io/#reference/forms/form-collection/create-a-draft-form) |
| [Create Draft Memo](actions/create-draft-memo.md) | `POST /memos` | [docs](https://sammapi.docs.apiary.io/#reference/memos/memo-collection/create-a-draft-memo) |
| [Get Action](actions/get-action.md) | `GET /actions/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/actions/action-instance/retrieve-an-action) |
| [Get Approver Type](actions/get-approver-type.md) | `GET /approver_types/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/approver-types/approver-type-instance/get-an-approver-type) |
| [Get Company](actions/get-company.md) | `GET /companies/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/companies/company-instance/retrieve-a-company) |
| [Get Drawing](actions/get-drawing.md) | `GET /drawings/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/drawings/drawing-instance/get-a-drawing) |
| [Get Form](actions/get-form.md) | `GET /forms/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/forms/form-instance/retrieve-a-form) |
| [Get Form Integration Representation](actions/get-form-integration-representation.md) | `GET /forms/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/forms/form-instance/retrieve-a-form) |
| [Get Memo](actions/get-memo.md) | `GET /memos/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/memos/memo-instance/retrieve-a-memo) |
| [Get Organisation](actions/get-organisation.md) | `GET /organisation/` | [docs](https://sammapi.docs.apiary.io/#reference/organisation/organisation-instance/retrieve-an-organisation) |
| [Get Organisation List](actions/get-organisation-list.md) | `GET /organisation_lists/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/organisation-lists/organisation-list-instance/get-an-organisation-list) |
| [Get Project](actions/get-project.md) | `GET /projects/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/projects/project-instance/get-a-project) |
| [Get Project List](actions/get-project-list.md) | `GET /projects/{project_id}/project_lists/{project_list_type_id}` | [docs](https://sammapi.docs.apiary.io/#reference/project-lists/project-list-instance/get-a-project-list) |
| [Get Project List Type](actions/get-project-list-type.md) | `GET /project_list_types/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/project-list-types/project-list-type-instance/get-a-project-list-type) |
| [Get Project Member](actions/get-project-member.md) | `GET /projects/{project_id}/project_members/{user_id}` | [docs](https://sammapi.docs.apiary.io/#reference/project-members/project-member-instance/get-a-project-member) |
| [Get Punch List](actions/get-punch-list.md) | `GET /punch_lists/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/punch-lists/punch-list-instance/get-a-punch-list) |
| [Get Submission Status](actions/get-submission-status.md) | `GET /submissions/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/submissions/submission-instance/check-the-status-of-a-submitted-request) |
| [Get Template](actions/get-template.md) | `GET /templates/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/templates/template-instance/retrieve-a-template) |
| [Get User](actions/get-user.md) | `GET /users/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/users/user-instance/retrieve-a-user) |
| [Get WBS Item](actions/get-wbs-item.md) | `GET /projects/{project_id}/wbs_items/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/wbs-items/wbs-item-instance/get-a-wbs-item) |
| [List Actions](actions/list-actions.md) | `GET /actions` | [docs](https://sammapi.docs.apiary.io/#reference/actions/action-collection/get-a-list-of-actions) |
| [List Approver Types](actions/list-approver-types.md) | `GET /approver_types` | [docs](https://sammapi.docs.apiary.io/#reference/approver-types/approver-type-collection/get-a-list-of-approver-types) |
| [List Drawing Annotations](actions/list-drawing-annotations.md) | `GET /drawing_annotations` | [docs](https://sammapi.docs.apiary.io/#reference/drawing-annotations/drawing-annotations-collection/get-a-list-of-drawing-annotations) |
| [List Drawing Views](actions/list-drawing-views.md) | `GET /drawing_views` | [docs](https://sammapi.docs.apiary.io/#reference/drawing-views/drawing-views-collection/get-a-list-of-drawing-views) |
| [List Drawings](actions/list-drawings.md) | `GET /drawings` | [docs](https://sammapi.docs.apiary.io/#reference/drawings/drawings-collection/get-a-list-of-drawings) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://sammapi.docs.apiary.io/#reference/forms/form-collection/get-a-list-of-forms) |
| [List Memos](actions/list-memos.md) | `GET /memos` | [docs](https://sammapi.docs.apiary.io/#reference/memos/memo-collection/get-a-list-of-memos) |
| [List Organisation Lists](actions/list-organisation-lists.md) | `GET /organisation_lists` | [docs](https://sammapi.docs.apiary.io/#reference/organisation-lists/organisation-list-collection/get-a-list-of-organisation-lists) |
| [List Project List Types](actions/list-project-list-types.md) | `GET /project_list_types` | [docs](https://sammapi.docs.apiary.io/#reference/project-list-types/project-list-type-collection/get-a-list-of-project-list-types) |
| [List Project Lists](actions/list-project-lists.md) | `GET /projects/{project_id}/project_lists` | [docs](https://sammapi.docs.apiary.io/#reference/project-lists/project-list-collection/get-a-list-of-project-lists) |
| [List Project Members](actions/list-project-members.md) | `GET /projects/{project_id}/project_members` | [docs](https://sammapi.docs.apiary.io/#reference/project-members/project-member-collection/get-a-list-of-project-members) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://sammapi.docs.apiary.io/#reference/projects/project-collection/get-a-list-of-projects) |
| [List Punch Lists](actions/list-punch-lists.md) | `GET /punch_lists` | [docs](https://sammapi.docs.apiary.io/#reference/punch-lists/punch-list-collection/get-a-list-of-punch-lists) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://sammapi.docs.apiary.io/#reference/templates/template-collection/get-a-list-of-templates) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://sammapi.docs.apiary.io/#reference/users/user-collection/get-a-list-of-users) |
| [List WBS Items](actions/list-wbs-items.md) | `GET /projects/{project_id}/wbs_items` | [docs](https://sammapi.docs.apiary.io/#reference/wbs-items/wbs-item-collection/get-a-list-of-project-wbs-items) |
| [Update Action](actions/update-action.md) | `PATCH /actions/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/actions/action-instance/update-an-action) |
| [Update Form](actions/update-form.md) | `PATCH /forms/{id}` | [docs](https://sammapi.docs.apiary.io/#reference/forms/form-instance/update-a-form) |
