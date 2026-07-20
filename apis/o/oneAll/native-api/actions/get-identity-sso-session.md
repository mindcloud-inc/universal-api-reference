# Get Identity SSO Session with OneAll

Retrieves an identity's SSO session from OneAll.

## Endpoint

- **Method:** `GET`
- **Path:** `/sso/sessions/identities/<identity_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Get Identity SSO Session](https://docs.oneall.com/api/resources/sso/identity/read-session/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_token` | path | `string` | yes | The OneAll identity token. |
