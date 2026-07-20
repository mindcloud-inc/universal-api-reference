# Form.io: Native API Reference

A consolidated summary of Form.io's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://help.form.io/developers/introduction/api-documentation
- **API base URL:** `https://neabnzbnvbushtk.form.io`

## Authentication

### Project API Key

Form.io project API key sent on the x-token header for administrative API requests.

### Credentials

- **API Key:** `apiKey` · required · Form.io project API key. MindCloud stores it as credentials.apiKey and injects it into the x-token header on every request.

Send these headers with each API request:

```http
x-token: <apiKey>
```

[Official authentication documentation](https://help.form.io/developers/introduction/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Admin Submission](actions/create-admin-submission.md) | `POST /admin/submission` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Create Form](actions/create-form.md) | `POST /form` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Create Form Action](actions/create-form-action.md) | `POST /form/:formId/action` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Create Form Submission](actions/create-form-submission.md) | `POST /form/:formId/submission` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Create Role](actions/create-role.md) | `POST /role` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Create Tag](actions/create-tag.md) | `POST /tag` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Create User Submission](actions/create-user-submission.md) | `POST /user/submission` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Delete Admin Submission](actions/delete-admin-submission.md) | `DELETE /admin/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Delete Form](actions/delete-form.md) | `DELETE /form/:id` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Delete Form Action](actions/delete-form-action.md) | `DELETE /form/:formId/action/:actionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Delete Form Submission](actions/delete-form-submission.md) | `DELETE /form/:formId/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Delete User Submission](actions/delete-user-submission.md) | `DELETE /user/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Admin Submission](actions/get-admin-submission.md) | `GET /admin/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Form](actions/get-form.md) | `GET /form/:id` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Form Action](actions/get-form-action.md) | `GET /form/:formId/action/:actionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Form Submission](actions/get-form-submission.md) | `GET /form/:formId/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Project](actions/get-project.md) | `GET /` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Project Access](actions/get-project-access.md) | `GET /access` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Project Token](actions/get-project-token.md) | `GET /token` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Role](actions/get-role.md) | `GET /role/:id` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get Tag](actions/get-tag.md) | `GET /tag/:tagId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Get User Submission](actions/get-user-submission.md) | `GET /user/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Admin Submissions](actions/list-admin-submissions.md) | `GET /admin/submission` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Form Actions](actions/list-form-actions.md) | `GET /form/:formId/action` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /form/:formId/submission` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Forms](actions/list-forms-all.md) | `GET /form` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Resource Forms](actions/list-resource-forms.md) | `GET /form` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Roles](actions/list-roles.md) | `GET /role` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Standard Forms](actions/list-standard-forms.md) | `GET /form` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List Tags](actions/list-tags.md) | `GET /tag` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [List User Submissions](actions/list-user-submissions.md) | `GET /user/submission` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Search Forms](actions/search-forms.md) | `GET /form` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Search Roles](actions/search-roles.md) | `GET /role` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Update Admin Submission](actions/update-admin-submission.md) | `PUT /admin/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Update Form](actions/update-form.md) | `PUT /form/:id` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Update Form Action](actions/update-form-action.md) | `PUT /form/:formId/action/:actionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Update Form Submission](actions/update-form-submission.md) | `PUT /form/:formId/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Update Role](actions/update-role.md) | `PUT /role/:id` | [docs](https://help.form.io/developers/introduction/api-documentation) |
| [Update User Submission](actions/update-user-submission.md) | `PUT /user/submission/:submissionId` | [docs](https://help.form.io/developers/introduction/api-documentation) |
