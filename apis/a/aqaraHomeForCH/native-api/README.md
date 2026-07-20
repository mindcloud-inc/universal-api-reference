# Aqara Home for CH: Native API Reference

A consolidated summary of Aqara Home for CH's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://opendoc.aqara.com/en/docs/developmanual/processOverview.html
- **API base URL:** `https://open-cn.aqara.com`

## Authentication

### Signed Open Platform

Use Aqara China Mainland app credentials plus authorization artifacts for signed Open Platform requests.

### Credentials

- **App ID:** `appId` · required · Aqara Open Platform AppId used in signed China Mainland requests.
- **Access Token:** `accessToken` · optional · Authorization access token returned by Aqara after account or project authorization.
- **App Key:** `appKey` · required · Aqara Open Platform AppKey used to derive the Sign header.
- **Refresh Token:** `refreshToken` · optional · Authorization refresh token returned by Aqara for renewing access.
- **Account Type:** `accountType` · optional · Aqara account type used for authorization code requests. Use the provider-documented value for email or phone account flows.
- **Account:** `account` · optional · Aqara account identifier used when requesting an authorization code; email or phone based on accountType.
- **Key ID:** `keyId` · required · Aqara Open Platform KeyId used in signed China Mainland requests.

[Official authentication documentation](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Position](actions/create-position.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Delete Position](actions/delete-position.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Get Access Token](actions/get-access-token.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html) |
| [Get Authorization Code](actions/get-authorization-code.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html) |
| [Get Position Details](actions/get-position-details.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [List Positions](actions/list-positions.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
| [Refresh Access Token](actions/refresh-access-token.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html) |
| [Update Position](actions/update-position.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html) |
