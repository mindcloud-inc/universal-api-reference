# Aqara Home for SG: Native API Reference

A consolidated summary of Aqara Home for SG's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html
- **API base URL:** `https://open-sg.aqara.com`

## Authentication

### Signed Request + Access Token

Uses Aqara SG signed request headers plus account authorization artifacts when required by the selected action.

### Credentials

- **App ID:** `appId` · required · Official Aqara application identifier for the SG project.
- **Key ID:** `keyId` · required · Official Aqara key identifier paired with the App Key.
- **App Key:** `appKey` · required · Official Aqara application secret used to generate the request signature.
- **Access Token:** `accessToken` · optional · Aqara account access token for endpoints that require account authorization.
- **Refresh Token:** `refreshToken` · optional · Refresh token returned by Get Access Token.
- **Open ID:** `openId` · optional · Authorized user unique identifier returned by Get Access Token.
- **Account:** `account` · optional · Aqara account (email or phone number) used to request and exchange the authorization code.
- **Auth Code:** `authCode` · optional · Authorization verification code from config.auth.getAuthCode. Aqara docs state it is valid for 10 minutes.

[Official authentication documentation](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html) |
| [Refresh Access Token](actions/refresh-access-token.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html) |
| [Request Auth Code](actions/request-auth-code.md) | `POST /v3.0/open/api` | [docs](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html) |
