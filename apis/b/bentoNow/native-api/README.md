# Bento Now: Native API Reference

A consolidated summary of Bento Now's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://bentonow.com/docs/
- **API base URL:** `https://app.bentonow.com/api`

## Authentication

### Basic Auth

Use your Bento publishable key, secret key, and site UUID.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Site UUID:** `siteUuid` · required · The Bento site UUID for the site to access.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://bentonow.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud/1.0` |

Response data is read from `data`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Broadcasts](actions/create-broadcasts.md) | `POST /v1/batch/broadcasts` | [docs](https://bentonow.com/docs/broadcasts) |
| [Create Emails](actions/create-emails.md) | `POST /v1/batch/emails` | [docs](https://bentonow.com/docs/emails_api) |
| [Create Events](actions/create-events.md) | `POST /v1/batch/events` | [docs](https://bentonow.com/docs/events_api) |
| [Create Field](actions/create-field.md) | `POST /v1/fetch/fields` | [docs](https://bentonow.com/docs/fields) |
| [Create Sequence Email](actions/create-sequence-email.md) | `POST /v1/fetch/sequences/:id/emails/templates` | [docs](https://bentonow.com/docs/sequences_api) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /v1/fetch/subscribers` | [docs](https://bentonow.com/docs/subscribers) |
| [Create Tag](actions/create-tag.md) | `POST /v1/fetch/tags` | [docs](https://bentonow.com/docs/tags_api) |
| [Find Subscriber](actions/find-subscriber.md) | `GET /v1/fetch/subscribers` | [docs](https://bentonow.com/docs/subscribers) |
| [Get Broadcasts](actions/get-broadcasts.md) | `GET /v1/fetch/broadcasts` | [docs](https://bentonow.com/docs/broadcasts) |
| [Get Email Template](actions/get-email-template.md) | `GET /v1/fetch/emails/templates/:id` | [docs](https://bentonow.com/docs/email_templates_api) |
| [Get Fields](actions/get-fields.md) | `GET /v1/fetch/fields` | [docs](https://bentonow.com/docs/fields) |
| [Get Segment Stats](actions/get-segment-stats.md) | `GET /v1/stats/segment` | [docs](https://bentonow.com/docs/stats) |
| [Get Sequences](actions/get-sequences.md) | `GET /v1/fetch/sequences` | [docs](https://bentonow.com/docs/sequences_api) |
| [Get Site Stats](actions/get-site-stats.md) | `GET /v1/stats/site` | [docs](https://bentonow.com/docs/stats) |
| [Get Tags](actions/get-tags.md) | `GET /v1/fetch/tags` | [docs](https://bentonow.com/docs/tags_api) |
| [Get Workflows](actions/get-workflows.md) | `GET /v1/fetch/workflows` | [docs](https://bentonow.com/docs/workflows_api) |
| [Import Subscribers](actions/import-subscribers.md) | `POST /v1/batch/subscribers` | [docs](https://bentonow.com/docs/subscribers) |
| [Run Subscriber Command](actions/run-subscriber-command.md) | `POST /v1/fetch/commands` | [docs](https://bentonow.com/docs/subscribers) |
| [Update Email Template](actions/update-email-template.md) | `PATCH /v1/fetch/emails/templates/:id` | [docs](https://bentonow.com/docs/email_templates_api) |
