# Telldus Live!: Native API Reference

A consolidated summary of Telldus Live!'s API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API
- **API base URL:** `https://pa-api.telldus.com`

## Authentication

### OAuth 1.0a

Connect using Telldus Live OAuth 1.0a consumer and access tokens.

### Credentials

- **Consumer Key:** `consumerKey` · required
- **Consumer Secret:** `consumerSecret` · required
- **Access Token:** `accessToken` · required
- **Token Secret:** `tokenSecret` · required
- **Realm:** `realm` · optional

OAuth 1.0a signs every request with the consumer key and secret plus the access token and token secret. Use an OAuth 1.0a client library to construct the `Authorization` header; the signature depends on the HTTP method, URL, and request parameters and should not be assembled as a static token.

[Official authentication documentation](https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API)

## API conventions

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | `GET /json/clients/list` | [docs](https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API) |
| [List Devices](actions/list-devices.md) | `GET /json/devices/list` | [docs](https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API) |
| [List Events](actions/list-events.md) | `GET /json/events/list` | [docs](https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API) |
| [List Modes](actions/list-modes.md) | `GET /json/modes/list` | [docs](https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API) |
| [List Rooms](actions/list-rooms.md) | `GET /json/rooms/list` | [docs](https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API) |
| [List Sensors](actions/list-sensors.md) | `GET /json/sensors/list` | [docs](https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API) |
