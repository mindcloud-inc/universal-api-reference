# Destroy Identity SSO Session with OneAll

Deletes an identity's SSO session from OneAll.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sso/sessions/identities/<identity_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Destroy Identity SSO Session](https://docs.oneall.com/api/resources/sso/identity/destroy-session/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_token` | path | `string` | yes | The OneAll identity token. |
