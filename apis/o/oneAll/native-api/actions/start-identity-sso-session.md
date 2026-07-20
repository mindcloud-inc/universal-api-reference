# Start Identity SSO Session with OneAll

Starts an SSO session for an identity in OneAll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sso/sessions/identities/<identity_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Start Identity SSO Session](https://docs.oneall.com/api/resources/sso/identity/start-session/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_token` | path | `string` | yes | The OneAll identity token. |
