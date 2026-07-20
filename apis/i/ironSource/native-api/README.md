# ironSource: Native API Reference

A consolidated summary of ironSource's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.unity.com/en-us/grow/levelplay/platform/api
- **API base URL:** `https://platform.ironsrc.com/`

## Authentication

### LevelPlay Bearer Token

Generate a 24-hour bearer token from your Unity LevelPlay / ironSource secret key and refresh token.

### Credentials

- **Secret Key:** `secretKey` · required · Your Unity LevelPlay / ironSource Secret Key from My Account.
- **Refresh Token:** `refreshToken` · required · Your Unity LevelPlay / ironSource Refresh Token from My Account.
- **Access Token:** `accessToken` · required · Paste the full JWT-style bearer token returned by the Get Bearer Token action. It has three dot-separated sections and is valid for 24 hours; do not use the short dashboard token value.

Send these headers with each API request:

```http
secretkey: <secretKey>
refreshToken: <refreshToken>
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://docs.unity.com/en-us/grow/levelplay/platform/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `resultsPerPage` in the query string to set the page size (default 5000; accepted range 1–5000). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ad Units](actions/create-ad-units.md) | `POST levelPlay/adUnits/v1/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/ad-units) |
| [Create Application](actions/create-application.md) | `POST partners/publisher/applications/v6` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/application) |
| [Create Mediation Groups](actions/create-mediation-groups.md) | `POST levelPlay/groups/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/groups) |
| [Create Network Instances](actions/create-network-instances.md) | `POST levelPlay/network/instances/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/instances-api-v4) |
| [Create Placements](actions/create-placements.md) | `POST partners/publisher/placements/v1` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/placements) |
| [Delete Mediation Groups](actions/delete-mediation-groups.md) | `DELETE levelPlay/groups/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/groups) |
| [Delete Network Instances](actions/delete-network-instances.md) | `DELETE levelPlay/network/instances/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/instances-api-v4) |
| [Delete Placement](actions/delete-placement.md) | `DELETE partners/publisher/placements/v1` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/placements) |
| [Get Ad Units](actions/get-ad-units.md) | `GET levelPlay/adUnits/v1/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/ad-units) |
| [Get Bearer Token](actions/get-bearer-token.md) | `GET partners/publisher/auth` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/authentication) |
| [Get Impression Level Revenue Report URL](actions/get-impression-level-revenue-report-url.md) | `GET partners/adRevenueMeasurements/v4` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/impression-level-revenue-server-side) |
| [Get Mediation Groups](actions/get-mediation-groups.md) | `GET levelPlay/groups/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/groups) |
| [Get Network Instances](actions/get-network-instances.md) | `GET levelPlay/network/instances/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/instances-api-v4) |
| [Get Placements](actions/get-placements.md) | `GET partners/publisher/placements/v1` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/placements) |
| [Get Reporting](actions/get-reporting.md) | `GET levelPlay/reporting/v1` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/reporting) |
| [Get User Ad Revenue Report URL](actions/get-user-ad-revenue-report-url.md) | `GET partners/userAdRevenue/v3` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/impression-level-revenue-server-side) |
| [List Applications](actions/list-applications.md) | `GET partners/publisher/applications/v6` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/application) |
| [Update Ad Units](actions/update-ad-units.md) | `PUT levelPlay/adUnits/v1/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/ad-units) |
| [Update Mediation Groups](actions/update-mediation-groups.md) | `PUT levelPlay/groups/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/groups) |
| [Update Network Instances](actions/update-network-instances.md) | `PUT levelPlay/network/instances/v4/:appKey` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/instances-api-v4) |
| [Update Placements](actions/update-placements.md) | `PUT partners/publisher/placements/v1` | [docs](https://docs.unity.com/en-us/grow/levelplay/platform/api/placements) |
