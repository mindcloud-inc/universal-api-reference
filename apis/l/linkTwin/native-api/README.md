# LinkTwin: Native API Reference

A consolidated summary of LinkTwin's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://linktw.in/developers
- **API base URL:** `https://linktw.in/api`

## Authentication

### API Key

Authenticate LinkTwin API requests with a Bearer API key from Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://linktw.in/automate-links-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 15). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Link To Collection](actions/assign-link-to-collection.md) | `POST /collection/:collectionid/assign/:itemid` | [docs](https://linktw.in/developers#assign-a-link-to-a-collection) |
| [Bulk Assign Links To Collection](actions/bulk-assign-links-to-collection.md) | `POST /collection/:id/links` | [docs](https://linktw.in/developers#bulk-assign-links-to-collection) |
| [Bulk Assign Links To Pixel](actions/bulk-assign-links-to-pixel.md) | `POST /pixel/:id/links` | [docs](https://linktw.in/developers#bulk-assign-links-to-pixel) |
| [Bulk Delete Links](actions/bulk-delete-links.md) | `POST /urls/delete` | [docs](https://linktw.in/developers#bulk-delete-links) |
| [Create Branded Domain](actions/create-branded-domain.md) | `POST /domain/add` | [docs](https://linktw.in/developers#create-a-branded-domain) |
| [Create Collection](actions/create-collection.md) | `POST /collection/add` | [docs](https://linktw.in/developers#create-a-collection) |
| [Create Link](actions/create-link.md) | `POST /url/add` | [docs](https://linktw.in/developers#create-a-link) |
| [Create Pixel](actions/create-pixel.md) | `POST /pixel/add` | [docs](https://linktw.in/developers#create-a-pixel) |
| [Create QR Code](actions/create-qr-code.md) | `POST /qr/add` | [docs](https://linktw.in/developers#create-a-qr-code) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /collection/:id/delete` | [docs](https://linktw.in/developers#delete-collection) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /domain/:id/delete` | [docs](https://linktw.in/developers#delete-domain) |
| [Delete Link](actions/delete-link.md) | `DELETE /url/:id/delete` | [docs](https://linktw.in/developers#delete-link) |
| [Delete Pixel](actions/delete-pixel.md) | `DELETE /pixel/:id/delete` | [docs](https://linktw.in/developers#delete-pixel) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /qr/:id/delete` | [docs](https://linktw.in/developers#delete-a-qr-code) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://linktw.in/developers) |
| [Get Collection](actions/get-collection.md) | `GET /collection/:id` | [docs](https://linktw.in/developers#get-single-collection) |
| [Get Link](actions/get-link.md) | `GET /url/:id` | [docs](https://linktw.in/developers#get-a-single-link) |
| [Get Pixel](actions/get-pixel.md) | `GET /pixel/:id` | [docs](https://linktw.in/developers#get-single-pixel) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qr/:id` | [docs](https://linktw.in/developers#get-a-single-qr-code) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://linktw.in/developers#list-collections) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://linktw.in/developers#list-all-domains) |
| [List Links](actions/list-links.md) | `GET /urls` | [docs](https://linktw.in/developers#list-links) |
| [List Pixels](actions/list-pixels.md) | `GET /pixels` | [docs](https://linktw.in/developers#list-pixels) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qr` | [docs](https://linktw.in/developers#list-qr-codes) |
| [Update Collection](actions/update-collection.md) | `PUT /collection/:id/update` | [docs](https://linktw.in/developers#update-collection) |
| [Update Domain](actions/update-domain.md) | `PUT /domain/:id/update` | [docs](https://linktw.in/developers#update-domain) |
| [Update Link](actions/update-link.md) | `PUT /url/:id/update` | [docs](https://linktw.in/developers#update-link) |
| [Update Pixel](actions/update-pixel.md) | `PUT /pixel/:id/update` | [docs](https://linktw.in/developers#update-pixel) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /qr/:id/update` | [docs](https://linktw.in/developers#update-qr-code) |
