# ReleaseNotes: Native API Reference

A consolidated summary of ReleaseNotes's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://releasenotes.elevio.help/en/categories/19331-api
- **API base URL:** `https://api.releasenotes.io/api/v1`

## Authentication

### API Key

Use a ReleaseNotes API token for authenticated requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://releasenotes.elevio.help/en/articles/87749-getting-started-with-the-api)

## API conventions

Response data is read from `data`. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add to Notes Feed](actions/add-to-notes-feed.md) | `POST /projects/:projectId/notesbucket/append` | [docs](https://releasenotes.elevio.help/en/articles/87754-adding-to-your-notes-feed) |
| [Create or Update Release](actions/create-or-update-release.md) | `POST /projects/:projectId/releases` | [docs](https://releasenotes.elevio.help/en/articles/87753-create-update-a-release) |
| [Create Webhook](actions/create-webhook.md) | `POST /projects/:projectId/webhooks` | [docs](https://releasenotes.elevio.help/en/articles/87801-webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /projects/:projectId/webhooks/:webhookId` | [docs](https://releasenotes.elevio.help/en/articles/87801-webhooks) |
| [Get Latest Release](actions/get-latest-release.md) | `GET /projects/:projectId/releases/latest` | [docs](https://releasenotes.elevio.help/en/articles/87752-retrieving-releases) |
| [Get Release](actions/get-release.md) | `GET /projects/:projectId/releases/:releaseId` | [docs](https://releasenotes.elevio.help/en/articles/87752-retrieving-releases) |
| [List Releases](actions/list-releases.md) | `GET /projects/:projectId/releases` | [docs](https://releasenotes.elevio.help/en/articles/87752-retrieving-releases) |
| [List Subscribers](actions/list-subscribers.md) | `GET /projects/:projectId/subscribers` | [docs](https://releasenotes.elevio.help/en/articles/87723-listing-subscribers) |
| [List Webhooks](actions/list-webhooks.md) | `GET /projects/:projectId/webhooks` | [docs](https://releasenotes.elevio.help/en/articles/87801-webhooks) |
| [Remove Subscriber](actions/remove-subscriber.md) | `POST /projects/:projectId/subscribers/remove` | [docs](https://releasenotes.elevio.help/en/articles/87725-deleting-a-subscriber) |
| [Search Subscribers](actions/search-subscribers.md) | `POST /projects/:projectId/subscribers/search` | [docs](https://releasenotes.elevio.help/en/articles/87724-searching-subscribers) |
