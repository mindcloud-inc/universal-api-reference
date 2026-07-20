# Revoke OAuth Access Token with RightSignature

Revokes a RightSignature OAuth access token.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.rightsignature.com/oauth/revoke`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Revoke OAuth Access Token](https://api.rightsignature.com/documentation/resources/v2/oauth_tokens/revoke.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | The access token to be revoked |
