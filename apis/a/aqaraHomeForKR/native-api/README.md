# Aqara Home for KR: Native API Reference

A consolidated summary of Aqara Home for KR's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html
- **API base URL:** `https://open-kr.aqara.com`

## Authentication

### Aqara Open Platform

Signed Aqara Open Platform requests for the South Korea region.

### Credentials

- **App ID:** `appId` · required · Aqara project Appid used in signed request headers.
- **App Key:** `appKey` · required · Aqara project AppKey used to generate the Sign header.
- **Key ID:** `keyId` · required · Aqara Keyid paired with the AppKey for signing.
- **Access Token:** `accessToken` · optional · Authorized Aqara access token used for protected KR APIs when present.
- **Refresh Token:** `refreshToken` · optional · Refresh token returned by Aqara authorization flows.
- **Open ID:** `openId` · optional · Authorized Aqara user or project identifier returned with token exchange responses.

[Official authentication documentation](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Position](actions/create-position.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Delete Position](actions/delete-position.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Get Position Details](actions/get-position-details.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [List Devices](actions/list-devices.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [List Gateway Subdevices](actions/list-gateway-subdevices.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [List Positions](actions/list-positions.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Rename Device](actions/rename-device.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html) |
| [Update Position](actions/update-position.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Update Position Timezone](actions/update-position-timezone.md) | `POST v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
