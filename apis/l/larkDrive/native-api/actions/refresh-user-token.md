# Refresh User Token with Lark Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/authen/v2/oauth/token`
- **Base URL:** `https://open.larksuite.com/open-apis`
- **Official documentation:** [Refresh User Token](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/authentication-management/access-token/refresh-user-access-token)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | body | `string` | yes | Lark refresh_token. Lark rotates it on each refresh, so always persist and reuse the latest returned value. |
