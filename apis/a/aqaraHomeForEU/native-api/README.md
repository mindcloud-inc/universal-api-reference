# Aqara Home for EU: Native API Reference

A consolidated summary of Aqara Home for EU's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://opendoc.aqara.cn/en/docs/developmanual/apiDocument.html
- **API base URL:** `https://open-ger.aqara.com`

## Authentication

### Signed Request + Access Token

Uses Aqara EU signed request headers plus account authorization artifacts when required by the selected action.

### Credentials

- **App ID:** `appId` · required · Official Aqara application identifier for the EU project.
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

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/config-auth-create-account.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/authManagement/virtualauthMode.html) |
| [Get Auth Code](actions/config-auth-get-auth-code.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/authManagement/virtualauthMode.html) |
| [Get Token](actions/config-auth-get-token.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/authManagement/virtualauthMode.html) |
| [Refresh Token](actions/config-auth-refresh-token.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/authManagement/virtualauthMode.html) |
| [Rename Device](actions/config-device-name.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Set Device Position](actions/config-device-position.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Create Linkage](actions/config-linkage-create.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/LinkageManagement.html) |
| [Delete Linkage](actions/config-linkage-delete.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/LinkageManagement.html) |
| [Enable Linkage](actions/config-linkage-enable.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/LinkageManagement.html) |
| [Update Linkage](actions/config-linkage-update.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/LinkageManagement.html) |
| [Update Resource Info](actions/config-resource-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Subscribe Resource](actions/config-resource-subscribe.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Unsubscribe Resource](actions/config-resource-unsubscribe.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Create Scene](actions/config-scene-create.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/SceneManagement.html) |
| [Get Resource History](actions/fetch-resource-history.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Get Resource Statistics](actions/fetch-resource-statistics.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Check Device Bind Status](actions/query-device-bind.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Get Device Bind Key](actions/query-device-bind-key.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Get Device Info](actions/query-device-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Get Sub-Device Info](actions/query-device-sub-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Get IFTTT Actions](actions/query-ifttt-action.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/Linkageconfiguration.html) |
| [Get IFTTT Triggers](actions/query-ifttt-trigger.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/Linkageconfiguration.html) |
| [Get Linkage Details](actions/query-linkage-detail.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/LinkageManagement.html) |
| [Get Resource Info](actions/query-resource-info.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Get Resource Name](actions/query-resource-name.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Get Resource Value](actions/query-resource-value.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
| [Disable Hub Subdevice Mode](actions/write-device-close-connect.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Enable Hub Subdevice Mode](actions/write-device-open-connect.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Unbind Device](actions/write-device-unbind.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Control Device Resource](actions/write-resource-device.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.cn/en/docs/developmanual/apiDocument/ResourceManagement.html) |
