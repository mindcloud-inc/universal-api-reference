# Weberlo: Native API Reference

A consolidated summary of Weberlo's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://developers.weberlo.com/
- **API base URL:** `https://connect.weberlo.com`

## Authentication

### API Key

Use your Weberlo API credential in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · Your Weberlo workspace ID.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.weberlo.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ad Channel](actions/create-ad-channel.md) | `POST /channel-ad` | [docs](https://developers.weberlo.com/#tag/Ad-Channels/paths/~1channel-ad/post) |
| [Create Channel](actions/create-channel.md) | `POST /channel` | [docs](https://developers.weberlo.com/#tag/Channels/paths/~1channel/post) |
| [Create Form Submit Event](actions/create-form-submit-event.md) | `POST /event/form` | [docs](https://developers.weberlo.com/#tag/Event/paths/~1event~1form/post) |
| [Create Transaction Event](actions/create-transaction-event.md) | `POST /event/transaction` | [docs](https://developers.weberlo.com/#tag/Event/paths/~1event~1transaction/post) |
| [Create UTM Channel](actions/create-utm-channel.md) | `POST /channel-utm` | [docs](https://developers.weberlo.com/#tag/UTM-Channel/paths/~1channel-utm/post) |
| [Delete Ad Channel](actions/delete-ad-channel.md) | `DELETE /channel-ad/:id` | [docs](https://developers.weberlo.com/#tag/Ad-Channels/paths/~1channel-ad~1{id}/delete) |
| [Delete Channel](actions/delete-channel.md) | `DELETE /channel/:id` | [docs](https://developers.weberlo.com/#tag/Channels/paths/~1channel~1{id}/delete) |
| [Delete UTM Channel](actions/delete-utm-channel.md) | `DELETE /channel-utm/:id` | [docs](https://developers.weberlo.com/#tag/UTM-Channel/paths/~1channel-utm~1{id}/delete) |
| [Get Ad Channel](actions/get-ad-channel.md) | `GET /channel-ad/:id` | [docs](https://developers.weberlo.com/#tag/Ad-Channels/paths/~1channel-ad~1{id}/get) |
| [Get UTM Channel](actions/get-utm-channel.md) | `GET /channel-utm/:id` | [docs](https://developers.weberlo.com/#tag/UTM-Channel/paths/~1channel-utm~1{id}/get) |
| [List Channels](actions/list-channels.md) | `GET /channel/list` | [docs](https://developers.weberlo.com/#tag/Channels/paths/~1channel~1list/get) |
| [List Persons](actions/list-persons.md) | `POST /person/list` | [docs](https://developers.weberlo.com/#tag/Person/paths/~1person~1list/post) |
| [List Visitors](actions/list-visitors.md) | `POST /visitor/list` | [docs](https://developers.weberlo.com/#tag/Visitor/paths/~1visitor~1list/post) |
| [List Websites](actions/list-websites.md) | `GET /page/website/list` | [docs](https://developers.weberlo.com/#tag/Page/paths/~1page~1website~1list/get) |
| [Search Pages](actions/search-pages.md) | `GET /page/search` | [docs](https://developers.weberlo.com/#tag/Page/paths/~1page~1search/get) |
| [Update Ad Channel](actions/update-ad-channel.md) | `PATCH /channel-ad/:id` | [docs](https://developers.weberlo.com/#tag/Ad-Channels/paths/~1channel-ad~1{id}/patch) |
| [Update UTM Channel](actions/update-utm-channel.md) | `PATCH /channel-utm/:id` | [docs](https://developers.weberlo.com/#tag/UTM-Channel/paths/~1channel-utm~1{id}/patch) |
