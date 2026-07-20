# Get SSO Session with OneAll

Retrieves SSO session details from OneAll.

## Endpoint

- **Method:** `GET`
- **Path:** `/sso/sessions/<sso_session_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Get SSO Session](https://docs.oneall.com/api/resources/sso/read-session-details/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sso_session_token` | path | `string` | yes | The OneAll SSO session token. |
