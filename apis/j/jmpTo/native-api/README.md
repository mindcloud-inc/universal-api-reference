# JmpTo: Native API Reference

A consolidated summary of JmpTo's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://jmpto.net/developers
- **API base URL:** `https://jmpto.net/api`

## Authentication

### API Key

Authenticate JmpTo API requests with the API key generated for the user account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://jmpto.net/developers)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Item to Channel](actions/assign-item-to-channel.md) | `POST /channel/:channelid/assign/:type/:itemid` | [docs](https://jmpto.net/developers#assign-an-item-to-a-channel) |
| [Assign Link to Campaign](actions/assign-link-to-campaign.md) | `POST /campaign/:campaignid/assign/:linkid` | [docs](https://jmpto.net/developers#assign-a-link-to-a-campaign) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaign/add` | [docs](https://jmpto.net/developers#create-a-campaign) |
| [Create Channel](actions/create-channel.md) | `POST /channel/add` | [docs](https://jmpto.net/developers#create-a-channel) |
| [Create Pixel](actions/create-pixel.md) | `POST /pixel/add` | [docs](https://jmpto.net/developers#create-a-pixel) |
| [Create QR Code](actions/create-qr-code.md) | `POST /qr/add` | [docs](https://jmpto.net/developers#create-a-qr-code) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaign/:id/delete` | [docs](https://jmpto.net/developers#delete-campaign) |
| [Delete Channel](actions/delete-channel.md) | `DELETE /channel/:id/delete` | [docs](https://jmpto.net/developers#delete-channel) |
| [Delete Link](actions/delete-link.md) | `DELETE /url/:id/delete` | [docs](https://jmpto.net/developers#delete-link) |
| [Delete Pixel](actions/delete-pixel.md) | `DELETE /pixel/:id/delete` | [docs](https://jmpto.net/developers#delete-pixel) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /qr/:id/delete` | [docs](https://jmpto.net/developers#delete-qr-code) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://jmpto.net/developers#get-account) |
| [Get Link](actions/get-link.md) | `GET /url/:id` | [docs](https://jmpto.net/developers#get-a-single-link) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qr/:id` | [docs](https://jmpto.net/developers#get-a-single-qr-code) |
| [List Branded Domains](actions/list-branded-domains.md) | `GET /domains` | [docs](https://jmpto.net/developers#list-branded-domains) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://jmpto.net/developers#list-campaigns) |
| [List Channel Items](actions/list-channel-items.md) | `GET /channel/:id` | [docs](https://jmpto.net/developers#list-channel-items) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://jmpto.net/developers#list-channels) |
| [List CTA Overlays](actions/list-cta-overlays.md) | `GET /overlay` | [docs](https://jmpto.net/developers#list-cta-overlays) |
| [List Custom Splash Pages](actions/list-custom-splash-pages.md) | `GET /splash` | [docs](https://jmpto.net/developers#list-custom-splash) |
| [List Links](actions/list-links.md) | `GET /urls` | [docs](https://jmpto.net/developers#list-links) |
| [List Pixels](actions/list-pixels.md) | `GET /pixels` | [docs](https://jmpto.net/developers#list-pixels) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qr` | [docs](https://jmpto.net/developers#list-qr-codes) |
| [Shorten Link](actions/shorten-link.md) | `POST /url/add` | [docs](https://jmpto.net/developers#shorten-a-link) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaign/:id/update` | [docs](https://jmpto.net/developers#update-campaign) |
| [Update Channel](actions/update-channel.md) | `PUT /channel/:id/update` | [docs](https://jmpto.net/developers#update-channel) |
| [Update Link](actions/update-link.md) | `PUT /url/:id/update` | [docs](https://jmpto.net/developers#update-link) |
| [Update Pixel](actions/update-pixel.md) | `PUT /pixel/:id/update` | [docs](https://jmpto.net/developers#update-pixel) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /qr/:id/update` | [docs](https://jmpto.net/developers#update-qr-code) |
