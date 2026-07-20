# 123FormBuild: Native API Reference

A consolidated summary of 123FormBuild's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.123formbuilder.com/developer/
- **OpenAPI specification:** https://www.123formbuilder.com/wp-content/uploads/sites/5/2024/01/swagger-4.json
- **API base URL:** `https://api.123formbuilder.com/v2`

## Authentication

### JWT Token

Use a 123FormBuilder JWT token generated from the API v2 authentication endpoint.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.123formbuilder.com/developer/api-v2-authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.pagination.total_pages`. The current page number is read from `meta.pagination.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 100; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://www.123formbuilder.com/developer/api-v2/) |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://www.123formbuilder.com/developer/api-v2-groups/) |
| [Create Subuser](actions/create-subuser.md) | `POST /users` | [docs](https://www.123formbuilder.com/developer/api-v2-users/) |
| [Delete Form](actions/delete-form.md) | `DELETE /forms/{form_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [Delete Multiple Forms](actions/delete-multiple-forms.md) | `DELETE /forms/bulk` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /forms/{form_id}/submissions/{submission_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [Get Form](actions/get-form.md) | `GET /forms/{form_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [Get Group](actions/get-group.md) | `GET /groups/{group_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-groups/) |
| [Get Submission](actions/get-submission.md) | `GET /forms/{form_id}/submissions/{submission_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [List Form Fields](actions/list-form-fields.md) | `GET /forms/{form_id}/fields` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [List Group Forms](actions/list-group-forms.md) | `GET /groups/{group_id}/forms` | [docs](https://www.123formbuilder.com/developer/api-v2-groups/) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://www.123formbuilder.com/developer/api-v2-groups/) |
| [List Submissions](actions/list-submissions.md) | `GET /forms/{form_id}/submissions` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.123formbuilder.com/developer/api-v2-users/) |
| [Share Group](actions/share-group.md) | `POST /groups/{group_id}/share` | [docs](https://www.123formbuilder.com/developer/api-v2-groups/) |
| [Unshare Group](actions/unshare-group.md) | `POST /groups/{group_id}/unshare` | [docs](https://www.123formbuilder.com/developer/api-v2-groups/) |
| [Update Account](actions/update-account.md) | `PUT /accounts/{user_id}` | [docs](https://www.123formbuilder.com/developer/api-v2/) |
| [Update Form](actions/update-form.md) | `PUT /forms/{form_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [Update Group](actions/update-group.md) | `PUT /groups/{group_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-groups/) |
| [Update Submission](actions/update-submission.md) | `PUT /forms/{form_id}/submissions/{submission_id}` | [docs](https://www.123formbuilder.com/developer/api-v2-forms/) |
| [Update User](actions/update-user.md) | `PUT /users/{identifier}` | [docs](https://www.123formbuilder.com/developer/api-v2-users/) |
