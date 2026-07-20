# Put.io: Native API Reference

A consolidated summary of Put.io's API configuration, with links to official documentation.

- **Official docs:** https://api.put.io/v2/docs
- **OpenAPI specification:** https://api.swaggerhub.com/apis/putio/putio/2.8.14?resolved=true
- **API base URL:** `https://api.put.io/v2`

## Authentication

### OAuth 2.0

Connect Put.io with OAuth 2.0 bearer access tokens.

### Credentials

- **Access Token:** `accessToken` · required · Put.io OAuth 2.0 bearer access token.
- **Redirect URI:** `redirectUri` · required · Registered redirect URI for the Put.io OAuth app.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.put.io/v2/oauth2/authenticate to approve access.
2. Exchange the returned authorization code with a POST request to https://api.put.io/v2/oauth2/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://api.put.io/v2/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.
