# UK Check VAT: Native API Reference

A consolidated summary of UK Check VAT's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://developer.service.hmrc.gov.uk/api-documentation/docs/api/service/vat-registered-companies-api/2.0
- **OpenAPI specification:** https://raw.githubusercontent.com/hmrc/vat-registered-companies-api/main/public/api/conf/2.0/application.yaml
- **API base URL:** `https://test-api.service.hmrc.gov.uk`

## Authentication

### HMRC OAuth2 Client Credentials

Authenticate to HMRC application-restricted endpoints using OAuth 2.0 client credentials.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://test-api.service.hmrc.gov.uk/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read:vat`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.service.hmrc.gov.uk/api-documentation/docs/authorisation/application-restricted-endpoints)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.hmrc.2.0+json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check VAT Registration](actions/check-vat-registration.md) | `GET /organisations/vat/check-vat-number/lookup/:targetVrn` | [docs](https://raw.githubusercontent.com/hmrc/vat-registered-companies-api/main/public/api/conf/2.0/application.yaml) |
| [Check VAT Registration With Reference Number](actions/check-vat-registration-with-reference-number.md) | `GET /organisations/vat/check-vat-number/lookup/:targetVrn/:requesterVrn` | [docs](https://raw.githubusercontent.com/hmrc/vat-registered-companies-api/main/public/api/conf/2.0/application.yaml) |
