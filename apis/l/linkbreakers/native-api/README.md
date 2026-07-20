# Linkbreakers: Native API Reference

A consolidated summary of Linkbreakers's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://linkbreakers.com/help/api
- **API base URL:** `https://api.linkbreakers.com`

## Authentication

### API Key

Authenticate with a Linkbreakers workspace token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://linkbreakers.com/help/article/how-to-use-the-linkbreakers-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `links`. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Shortlink Availability](actions/check-shortlink-availability.md) | `GET /v1/links/shortlink-availability` | [docs](https://linkbreakers.com/help/api/links) |
| [Create a Directory](actions/create-directory.md) | `POST /v1/directories` | [docs](https://linkbreakers.com/help/api/directories) |
| [Create Multiple Links](actions/create-multiple-links.md) | `POST /v1/links/bulk` | [docs](https://linkbreakers.com/help/api/links) |
| [Create a New Contact Card Link](actions/create-new-contact-card-link.md) | `POST /v1/links/contact` | [docs](https://linkbreakers.com/help/api/links) |
| [Create a New Link](actions/create-new-link.md) | `POST /v1/links` | [docs](https://linkbreakers.com/help/api/links) |
| [Create a New Workflow Step](actions/create-new-workflow-step.md) | `POST /v1/links/:linkId/workflow-steps` | [docs](https://linkbreakers.com/help/api/workflow-steps) |
| [Create a Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://linkbreakers.com/help/api/webhooks) |
| [Delete a Link](actions/delete-link.md) | `DELETE /v1/links/:id` | [docs](https://linkbreakers.com/help/api/links) |
| [Get Link Details](actions/get-link-details.md) | `GET /v1/links/:id` | [docs](https://linkbreakers.com/help/api/links) |
| [Get a Visitor](actions/get-visitor.md) | `GET /v1/visitors/:id` | [docs](https://linkbreakers.com/help/api/visitors) |
| [Identify Visitor](actions/identify-visitor.md) | `POST /v1/visitor/identify` | [docs](https://linkbreakers.com/help/api/visitors) |
| [List Directories](actions/list-directories.md) | `GET /v1/directories` | [docs](https://linkbreakers.com/help/api/directories) |
| [List Event Traces](actions/list-event-traces.md) | `GET /v1/events/:eventId/traces` | [docs](https://linkbreakers.com/help/api/events) |
| [List Events](actions/list-events.md) | `GET /v1/events` | [docs](https://linkbreakers.com/help/api/events) |
| [List Links](actions/list-links.md) | `GET /v1/links` | [docs](https://linkbreakers.com/help/api/links#list-links) |
| [List Media Files](actions/list-media-files.md) | `GET /v1/media` | [docs](https://linkbreakers.com/help/api/media) |
| [List Visitors](actions/list-visitors.md) | `GET /v1/visitors` | [docs](https://linkbreakers.com/help/api/visitors) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://linkbreakers.com/help/api/webhooks) |
| [List Workflow Steps for a Link](actions/list-workflow-steps-for-a-link.md) | `GET /v1/links/:linkId/workflow-steps` | [docs](https://linkbreakers.com/help/api/workflow-steps) |
| [Update a Directory](actions/update-directory.md) | `PATCH /v1/directories/:id` | [docs](https://linkbreakers.com/help/api/directories) |
| [Update a Link](actions/update-link.md) | `PATCH /v1/links/:id` | [docs](https://linkbreakers.com/help/api/links) |
| [Update a Visitor](actions/update-visitor.md) | `PATCH /v1/visitors/:id` | [docs](https://linkbreakers.com/help/api/visitors) |
| [Update a Webhook](actions/update-webhook.md) | `PATCH /v1/webhooks/:id` | [docs](https://linkbreakers.com/help/api/webhooks) |
| [Upload a Media File](actions/upload-media-file.md) | `POST /v1/media` | [docs](https://linkbreakers.com/help/api/media) |
