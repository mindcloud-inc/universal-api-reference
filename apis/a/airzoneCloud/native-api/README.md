# Airzone Cloud: Native API Reference

A consolidated summary of Airzone Cloud's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developers.airzonecloud.com/docs/web-api/
- **OpenAPI specification:** https://developers.airzonecloud.com/downloads/webapi.openapi.yml
- **API base URL:** `https://m.airzonecloud.com/api/v1`

## Authentication

### Bearer Token

Use an Airzone Cloud JWT access token. Airzone issues the token through its non-OAuth login flow, then operational requests use Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.airzonecloud.com/docs/web-api/)

## Pagination

Use `items` in the query string to set the page size (default 10; accepted range 1–10). Use `page` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Session Token Pair](actions/create-session-token-pair.md) | `POST /auth/login` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Get Current User](actions/get-current-user.md) | `GET /user/` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Get Device Configuration](actions/get-device-configuration.md) | `GET /devices/{deviceId}/config` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Get Device Status](actions/get-device-status.md) | `GET /devices/{deviceId}/status` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Get Installation](actions/get-installation.md) | `GET /installations/{installationId}` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Get Installation Location](actions/get-installation-location.md) | `GET /installations/location/{locationId}` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Get Webserver Status](actions/get-webserver-status.md) | `GET /devices/ws/{wsId}/status` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [List Installations](actions/list-installations.md) | `GET /installations` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Logout User](actions/logout-user.md) | `GET /user/logout` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Refresh Session Token Pair](actions/refresh-session-token-pair.md) | `GET /auth/refreshToken/{refreshToken}` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Update Device Parameter](actions/update-device-parameter.md) | `PATCH /devices/{deviceId}` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Update Installation](actions/update-installation.md) | `PUT /installations/{installationId}` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
| [Update Installation Group](actions/update-installation-group.md) | `PUT /installations/{installationId}/group/{groupId}` | [docs](https://developers.airzonecloud.com/docs/web-api/) |
