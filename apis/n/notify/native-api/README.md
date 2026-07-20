# Notify: Native API Reference

A consolidated summary of Notify's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://notify.run
- **API base URL:** `https://notify.run`

## Authentication

### Channel Token

Use a Notify channel token. Runtime requests inject the token into the request path, for example https://notify.run/{channelToken} .

### Credentials

- **Channel Token:** `channelToken` · optional · The channel token segment from your Notify endpoint URL, for example the token in https://notify.run/<token>.

[Official authentication documentation](https://notify.run)

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | `POST /register_channel` | [docs](https://notify.run) |
| [Get Channel Endpoint URL](actions/get-channel-endpoint-url.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [Get Channel Info](actions/get-channel-info.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [Get Channel Page URL](actions/get-channel-page-url.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [Get Channel Public Key](actions/get-channel-public-key.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [Get Channel QR Code](actions/get-channel-qr-code.md) | `GET /:channelId/qr.svg` | [docs](https://notify.run) |
| [Get Channel URLs](actions/get-channel-ur-ls.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [Get Current Channel Endpoint URL](actions/get-current-channel-endpoint-url.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [Get Current Channel Info](actions/get-current-channel-info.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [Get Current Channel Page URL](actions/get-current-channel-page-url.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [Get Current Channel Public Key](actions/get-current-channel-public-key.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [Get Current Channel QR Code](actions/get-current-channel-qr-code.md) | `GET /{{credentials.channelToken}}/qr.svg` | [docs](https://notify.run) |
| [Get Current Channel URLs](actions/get-current-channel-ur-ls.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [Get Latest Channel Message](actions/get-latest-channel-message.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [Get Latest Current Channel Message](actions/get-latest-current-channel-message.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [List Channel Delivery Results](actions/list-channel-delivery-results.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [List Channel Messages](actions/list-channel-messages.md) | `GET /:channelId/json` | [docs](https://notify.run) |
| [List Current Channel Delivery Results](actions/list-current-channel-delivery-results.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [List Current Channel Messages](actions/list-current-channel-messages.md) | `GET /{{credentials.channelToken}}/json` | [docs](https://notify.run) |
| [Send Channel Message](actions/send-channel-message.md) | `POST /:channelId` | [docs](https://notify.run) |
| [Send Current Channel Message](actions/send-current-channel-message.md) | `POST /{{credentials.channelToken}}` | [docs](https://notify.run) |
