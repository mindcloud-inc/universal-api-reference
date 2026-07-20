# Youform: Native API Reference

A consolidated summary of Youform's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://youform.com/api-docs
- **API base URL:** `https://app.youform.com/api`

## Authentication

### API Key

Use a bearer API token created from your Youform account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://go.postman.co/collection/21094175-e04cd7f9-1c88-471b-849b-0aba7be6c811?source=collection_link)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.last_page`. The current page number is read from `data.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://youform.com/api-docs) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://youform.com/api-docs) |
| [Get Form](actions/get-form.md) | `GET /forms/:formSlug` | [docs](https://youform.com/api-docs) |
| [Get My Profile](actions/get-my-profile.md) | `GET /me` | [docs](https://youform.com/api-docs) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /forms/:formSlug/submissions` | [docs](https://youform.com/api-docs) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://youform.com/api-docs) |
| [Set Submission Refill Link](actions/set-submission-refill-link.md) | `POST /submissions/:submissionId/refill-link` | [docs](https://youform.com/api-docs) |
