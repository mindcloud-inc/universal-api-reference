# Request OAuth Access Token with RightSignature

Requests a RightSignature OAuth access token.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.rightsignature.com/oauth/token`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Request OAuth Access Token](https://api.rightsignature.com/documentation/resources/v2/oauth_tokens/create.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | yes | The API Key's Client ID |
| `client_secret` | body | `string` | yes | The API Key's Client Secret |
| `redirect_uri` | body | `string` | yes | The API Key's redirect uri that was used in the authorization grant request |
| `code` | body | `string` | yes | The code that was included as a param in the redirect after authorizing |
