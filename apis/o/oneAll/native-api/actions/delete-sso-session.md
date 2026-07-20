# Delete SSO Session with OneAll

Deletes an SSO session from OneAll.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sso/sessions/<sso_session_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Delete SSO Session](https://docs.oneall.com/api/resources/sso/delete-session/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sso_session_token` | path | `string` | yes | The OneAll SSO session token. |
