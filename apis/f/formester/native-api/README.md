# Formester: Native API Reference

A consolidated summary of Formester's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.formester.com/formester-api-v2
- **API base URL:** `https://app.formester.com/api/v2`

## Authentication

### API Key

Connect using a Formester API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.formester.com/formester-api-v2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `meta.page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Submission](actions/delete-submission.md) | `DELETE /submissions/:id` | [docs](https://docs.formester.com/formester-api-v2#delete-submission) |
| [Get Submission](actions/get-submission.md) | `GET /submissions/:id` | [docs](https://docs.formester.com/formester-api-v2#get-submission) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://docs.formester.com/formester-api-v2#list-forms) |
| [List Submissions](actions/list-submissions.md) | `GET /submissions` | [docs](https://docs.formester.com/formester-api-v2#list-submissions) |
