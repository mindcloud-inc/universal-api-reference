# SendMails: Native API Reference

A consolidated summary of SendMails's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://sendmails.io/docs/campaigns-apis-by-sendmails-io/
- **API base URL:** `https://app.sendmails.io/api/v1`

## Authentication

### API Key

Use your SendMails Campaign API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.sendmails.io/frontend/docs/api/v1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add List Field](actions/add-list-field.md) | `POST /lists/:uid/add-field` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#3-toc-title) |
| [Add Subscriber Tags](actions/add-subscriber-tags.md) | `POST /subscribers/:uid/add-tag` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#3-toc-title) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /subscribers` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaigns/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#3-toc-title) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Find Subscribers By Email](actions/find-subscribers-by-email.md) | `GET /subscribers/email/:email` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Get Campaigns](actions/get-campaigns.md) | `GET /campaigns` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Get List](actions/get-list.md) | `GET /lists/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#3-toc-title) |
| [Get Lists](actions/get-lists.md) | `GET /lists` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#3-toc-title) |
| [Get Login Token](actions/get-login-token.md) | `POST /login-token` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#2-toc-title) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Get Subscribers](actions/get-subscribers.md) | `GET /subscribers` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /campaigns/:uid/pause` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Resume Campaign](actions/resume-campaign.md) | `POST /campaigns/:uid/resume` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Run Campaign](actions/run-campaign.md) | `POST /campaigns/:uid/run` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Subscribe Subscriber](actions/subscribe-subscriber.md) | `PATCH /lists/:list_uid/subscribers/:uid/subscribe` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `PATCH /lists/:list_uid/subscribers/:uid/unsubscribe` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /subscribers/:uid` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#5-toc-title) |
| [Upload File By Url](actions/upload-file-by-url.md) | `POST /file/upload` | [docs](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#7-toc-title) |
