# Plaid: Native API Reference

A consolidated summary of Plaid's API configuration, with links to official documentation.

- **Official docs:** https://plaid.com/docs/api/
- **OpenAPI specification:** https://raw.githubusercontent.com/plaid/plaid-openapi/master/2020-09-14.yml
- **API base URL:** `https://sandbox.plaid.com`

## Authentication

### Client ID + Secret

Use your Plaid client ID and secret for server-side API calls.

### Credentials

- **Client ID:** `clientId` · required · Your Plaid client_id from the Plaid Dashboard keys page.
- **Secret:** `secret` · required · Your Plaid secret for the selected environment.

[Official authentication documentation](https://plaid.com/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
