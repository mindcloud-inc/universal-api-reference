# Recut URL Shortener: Native API Reference

A consolidated summary of Recut URL Shortener's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://app.recut.in/developers
- **API base URL:** `https://app.recut.in/api`

## Authentication

### API key

Authenticate with a Recut API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.recut.in/developers)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Only one sort field is accepted.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Item To Channel](actions/assign-item-to-channel.md) | `POST /channel/:channelid/assign/:type/:itemid` | [docs](https://app.recut.in/developers#assign-an-item-to-a-channel) |
| [Assign Link To Campaign](actions/assign-link-to-campaign.md) | `POST /campaign/:campaignid/assign/:linkid` | [docs](https://app.recut.in/developers#assign-a-link-to-a-campaign) |
| [Create Branded Domain](actions/create-branded-domain.md) | `POST /domain/add` | [docs](https://app.recut.in/developers#create-a-branded-domain) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaign/add` | [docs](https://app.recut.in/developers#create-a-campaign) |
| [Create Channel](actions/create-channel.md) | `POST /channel/add` | [docs](https://app.recut.in/developers#create-a-channel) |
| [Create Pixel](actions/create-pixel.md) | `POST /pixel/add` | [docs](https://app.recut.in/developers#create-a-pixel) |
| [Create QR Code](actions/create-qr-code.md) | `POST /qr/add` | [docs](https://app.recut.in/developers#create-a-qr-code) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaign/:id/delete` | [docs](https://app.recut.in/developers#delete-campaign) |
| [Delete Channel](actions/delete-channel.md) | `DELETE /channel/:id/delete` | [docs](https://app.recut.in/developers#delete-channel) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /domain/:id/delete` | [docs](https://app.recut.in/developers#delete-domain) |
| [Delete Link](actions/delete-link.md) | `DELETE /url/:id/delete` | [docs](https://app.recut.in/developers#delete-a-link) |
| [Delete Pixel](actions/delete-pixel.md) | `DELETE /pixel/:id/delete` | [docs](https://app.recut.in/developers#delete-pixel) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /qr/:id/delete` | [docs](https://app.recut.in/developers#delete-a-qr-code) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://app.recut.in/developers) |
| [Get Link](actions/get-link.md) | `GET /url/:id` | [docs](https://app.recut.in/developers#get-a-single-link) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qr/:id` | [docs](https://app.recut.in/developers#get-a-single-qr-code) |
| [List Branded Domains](actions/list-branded-domains.md) | `GET /domains` | [docs](https://app.recut.in/developers#list-branded-domains) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://app.recut.in/developers#list-campaigns) |
| [List Channel Items](actions/list-channel-items.md) | `GET /channel/:id` | [docs](https://app.recut.in/developers#list-channel-items) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://app.recut.in/developers#list-channels) |
| [List CTA Overlays](actions/list-cta-overlays.md) | `GET /overlay` | [docs](https://app.recut.in/developers#list-cta-overlays) |
| [List Custom Splash](actions/list-custom-splash.md) | `GET /splash` | [docs](https://app.recut.in/developers#list-custom-splash) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://app.recut.in/developers#list-files) |
| [List Links](actions/list-links.md) | `GET /urls` | [docs](https://app.recut.in/developers#list-links) |
| [List Pixels](actions/list-pixels.md) | `GET /pixels` | [docs](https://app.recut.in/developers#list-pixels) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qr` | [docs](https://app.recut.in/developers#list-qr-codes) |
| [Shorten Link](actions/shorten-link.md) | `POST /url/add` | [docs](https://app.recut.in/developers#shorten-a-link) |
| [Update Account](actions/update-account.md) | `PUT /account/update` | [docs](https://app.recut.in/developers#update-account) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaign/:id/update` | [docs](https://app.recut.in/developers#update-campaign) |
| [Update Channel](actions/update-channel.md) | `PUT /channel/:id/update` | [docs](https://app.recut.in/developers#update-channel) |
| [Update Domain](actions/update-domain.md) | `PUT /domain/:id/update` | [docs](https://app.recut.in/developers#update-domain) |
| [Update Link](actions/update-link.md) | `PUT /url/:id/update` | [docs](https://app.recut.in/developers#update-link) |
| [Update Pixel](actions/update-pixel.md) | `PUT /pixel/:id/update` | [docs](https://app.recut.in/developers#update-pixel) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /qr/:id/update` | [docs](https://app.recut.in/developers#update-qr-code) |
| [Upload File](actions/upload-file.md) | `POST /files/upload/:filename` | [docs](https://app.recut.in/developers#upload-a-file) |
