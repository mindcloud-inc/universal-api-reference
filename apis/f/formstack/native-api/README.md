# Formstack: Native API Reference

A consolidated summary of Formstack's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.formstack.com/reference/overview
- **API base URL:** `https://www.formstack.com/api/v2025`

## Authentication

### API Key

Authenticate Formstack with a Personal Access Token (PAT).

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.formstack.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `page.totalPages`. The current page number is read from `page.pageNumber`.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 10–500). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `order`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Form](actions/copy-form.md) | `POST /forms/:formId/copy` | [docs](https://developers.formstack.com/reference/copyform-1) |
| [Count Form Submissions](actions/count-form-submissions.md) | `GET /forms/:formId/submissions/count` | [docs](https://developers.formstack.com/reference/countformsubmissions-1) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://developers.formstack.com/reference/createfolder-1) |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://developers.formstack.com/reference/createform-1) |
| [Create Form Field](actions/create-form-field.md) | `POST /forms/:formId/fields` | [docs](https://developers.formstack.com/reference/createfieldinform-1) |
| [Create Form Prefill URL](actions/create-form-prefill-url.md) | `POST /forms/:formId/prefill` | [docs](https://developers.formstack.com/reference/createformprefill-1) |
| [Create Submission](actions/create-submission.md) | `POST /forms/:formId/submissions` | [docs](https://developers.formstack.com/reference/createsubmission-1) |
| [Delete Form](actions/delete-form.md) | `DELETE /forms/:formId` | [docs](https://developers.formstack.com/reference/deleteform-1) |
| [Delete Form Field](actions/delete-form-field.md) | `DELETE /forms/:formId/fields/:fieldId` | [docs](https://developers.formstack.com/reference/deletefield-1) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /submissions/:submissionId` | [docs](https://developers.formstack.com/reference/deletesubmission-1) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:folderId` | [docs](https://developers.formstack.com/reference/getfolder-1) |
| [Get Form](actions/get-form.md) | `GET /forms/:formId` | [docs](https://developers.formstack.com/reference/getformdetails-1) |
| [Get Form Field](actions/get-form-field.md) | `GET /forms/:formId/fields/:fieldId` | [docs](https://developers.formstack.com/reference/getfielddetails-1) |
| [Get Form HTML](actions/get-form-html.md) | `GET /forms/:formId/html` | [docs](https://developers.formstack.com/reference/getformhtml-1) |
| [Get Submission](actions/get-submission.md) | `GET /submissions/:submissionId` | [docs](https://developers.formstack.com/reference/getsubmissiondetails-1) |
| [Get Submission Upload](actions/get-submission-upload.md) | `GET /submissions/:submissionId/upload` | [docs](https://developers.formstack.com/reference/getsubmissionupload-1) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://developers.formstack.com/reference/listfolders-1) |
| [List Form Fields](actions/list-form-fields.md) | `GET /forms/:formId/fields` | [docs](https://developers.formstack.com/reference/getformfields-1) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /forms/:formId/submissions` | [docs](https://developers.formstack.com/reference/getformsubmissionslist-1) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://developers.formstack.com/reference/getformslist-1) |
| [List Submissions](actions/list-submissions.md) | `GET /submissions` | [docs](https://developers.formstack.com/reference/getsubmissionslist-1) |
| [Update Form](actions/update-form.md) | `PUT /forms/:formId` | [docs](https://developers.formstack.com/reference/editform-1) |
| [Update Form Field](actions/update-form-field.md) | `PUT /forms/:formId/fields/:fieldId` | [docs](https://developers.formstack.com/reference/editfield-1) |
| [Update Submission](actions/update-submission.md) | `PUT /submissions/:submissionId` | [docs](https://developers.formstack.com/reference/editsubmission-1) |
