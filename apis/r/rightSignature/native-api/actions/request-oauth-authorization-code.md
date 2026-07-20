# Request OAuth Authorization Code with RightSignature

Requests a RightSignature OAuth authorization code.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.rightsignature.com/oauth/authorize`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Request OAuth Authorization Code](https://api.rightsignature.com/documentation/resources/v2/oauth_authorizations/default_url_options.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `string` | yes | The API Key's Client ID |
| `redirect_uri` | query | `string` | yes | Where the user-agent will be redirected to after an authorization code is granted. Note that this MUST match what is on record with the API Key associated with the passed in client id |
| `response_type` | query | `string` | yes | Requests the authorization code grant |
| `scope` | query | `string` | no | Level of access that the application is requesting. |
