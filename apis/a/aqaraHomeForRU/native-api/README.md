# Aqara Home for RU: Native API Reference

A consolidated summary of Aqara Home for RU's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html
- **API base URL:** `https://open-ru.aqara.com`

## Authentication

### Signed Request + Access Token

Uses Aqara RU signed request headers plus account authorization artifacts when required by the selected action.

### Credentials

- **App ID:** `appId` · required · Official Aqara application identifier for the RU project.
- **Key ID:** `keyId` · required · Official Aqara key identifier paired with the App Key.
- **App Key:** `appKey` · required · Official Aqara application secret used to generate the request signature.
- **Access Token:** `accessToken` · optional · Aqara account access token for endpoints that require account authorization.
- **Refresh Token:** `refreshToken` · optional · Refresh token returned by Get Access Token.
- **Open ID:** `openId` · optional · Authorized user unique identifier returned by Get Access Token.

[Official authentication documentation](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Update Device Name](actions/config-device-name.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Update Device Position](actions/config-device-position.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Create Linkage](actions/config-linkage-create.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Delete Linkage](actions/config-linkage-delete.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Enable Linkage](actions/config-linkage-enable.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Update Linkage](actions/config-linkage-update.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Create Position](actions/config-position-create.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Delete Position](actions/config-position-delete.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Update Position Time Zone](actions/config-position-time-zone.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Update Position](actions/config-position-update.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Update Resource Info](actions/config-resource-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Subscribe Resource](actions/config-resource-subscribe.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Unsubscribe Resource](actions/config-resource-unsubscribe.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Create Scene](actions/config-scene-create.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Run Scene](actions/config-scene-run.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Update Scene](actions/config-scene-update.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Fetch Resource History](actions/fetch-resource-history.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Fetch Resource Statistics](actions/fetch-resource-statistics.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Device Info](actions/query-device-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Sub-Device Info](actions/query-device-sub-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query IFTTT Actions](actions/query-ifttt-action.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query IFTTT Triggers](actions/query-ifttt-trigger.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Linkage Detail](actions/query-linkage-detail.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [List Linkages by Position](actions/query-linkage-list-by-position-id.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [List Linkages by Subject](actions/query-linkage-list-by-subject-id.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Position Detail](actions/query-position-detail.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Position Info](actions/query-position-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Resource Info](actions/query-resource-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Resource Name](actions/query-resource-name.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
| [Query Resource Value](actions/query-resource-value.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/requestIntent.html) |
