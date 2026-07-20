# Userback: Native API Reference

A consolidated summary of Userback's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.userback.io/reference
- **API base URL:** `https://rest.userback.io/1.0`

## Authentication

### API Token

Authenticate with a Userback workspace REST API token.

### Credentials

- **API Key:** `apiKey` · required
- **Partner Code:** `partnerCode` · optional · Optional Userback partner code for approved partner API access.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.userback.io/en/articles/9417164-rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `_pagination.totalPages`. The current page number is read from `_pagination.pageNumber`.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `ge`, `gt`, `le`, `lt`, `ne`.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | `POST /feedback` | [docs](https://docs.userback.io/reference/createfeedback) |
| [Create Feedback Comment](actions/create-feedback-comment.md) | `POST /feedback/comment` | [docs](https://docs.userback.io/reference/createfeedbackcomment) |
| [Create Feedback Screenshot](actions/create-feedback-screenshot.md) | `POST /feedback/screenshot` | [docs](https://docs.userback.io/reference/createscreenshot) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflow` | [docs](https://docs.userback.io/reference/createworkflow) |
| [Delete Feedback](actions/delete-feedback.md) | `DELETE /feedback/:id` | [docs](https://docs.userback.io/reference/deletefeedback) |
| [Delete Feedback Comment](actions/delete-feedback-comment.md) | `DELETE /feedback/comment/:id` | [docs](https://docs.userback.io/reference/deletefeedbackcomment) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /workflow/:id` | [docs](https://docs.userback.io/reference/deleteworkflow) |
| [Get Feedback](actions/get-feedback.md) | `GET /feedback/:id` | [docs](https://docs.userback.io/reference/getfeedback) |
| [Get Feedback Comment](actions/get-feedback-comment.md) | `GET /feedback/comment/:id` | [docs](https://docs.userback.io/reference/getfeedbackcomment) |
| [Get Member](actions/get-member.md) | `GET /member/:id` | [docs](https://docs.userback.io/reference/getmember) |
| [Get Project](actions/get-project.md) | `GET /project/:id` | [docs](https://docs.userback.io/reference/getproject) |
| [Get Session Recording](actions/get-session-recording.md) | `GET /sessionRecording/:id` | [docs](https://docs.userback.io/reference/getsessionrecording) |
| [List Feedback Comments](actions/list-feedback-comments.md) | `GET /feedback/comment` | [docs](https://docs.userback.io/reference/listfeedbackcomments) |
| [List Feedbacks](actions/list-feedbacks.md) | `GET /feedback` | [docs](https://docs.userback.io/reference/listfeedbacks) |
| [List Members](actions/list-members.md) | `GET /member` | [docs](https://docs.userback.io/reference/listmembers) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://docs.userback.io/reference/listprojects) |
| [List Session Recordings](actions/list-session-recordings.md) | `GET /sessionRecording` | [docs](https://docs.userback.io/reference/listsessionrecordings) |
| [List Workflows](actions/list-workflows.md) | `GET /workflow` | [docs](https://docs.userback.io/reference/listworkflows) |
| [Update Feedback](actions/update-feedback.md) | `PATCH /feedback/:id` | [docs](https://docs.userback.io/reference/updatefeedback) |
| [Update Feedback Comment](actions/update-feedback-comment.md) | `PATCH /feedback/comment/:id` | [docs](https://docs.userback.io/reference/updatefeedbackcomment) |
| [Update Member](actions/update-member.md) | `PATCH /member/:id` | [docs](https://docs.userback.io/reference/updatemember) |
| [Update Project](actions/update-project.md) | `PATCH /project/:id` | [docs](https://docs.userback.io/reference/updateproject) |
| [Update Workflow](actions/update-workflow.md) | `PATCH /workflow/:id` | [docs](https://docs.userback.io/reference/updateworkflow) |
