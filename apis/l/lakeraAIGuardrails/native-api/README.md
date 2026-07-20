# Lakera AI Guardrails: Native API Reference

A consolidated summary of Lakera AI Guardrails's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.lakera.ai/docs/api
- **OpenAPI specification:** https://docs.lakera.ai/api-reference
- **API base URL:** `https://api.lakera.ai/v2`

## Authentication

### Bearer API Key

Lakera API key sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.lakera.ai/docs/quickstart)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Policy Health](actions/check-policy-health.md) | `POST /policies/health` | [docs](https://docs.lakera.ai/api-reference/lakera-api/policies-health/check-policy-health) |
| [Get Detailed Detector Results](actions/get-detailed-detector-results.md) | `POST /guard/results` | [docs](https://docs.lakera.ai/api-reference/lakera-api/guard-results/get-results) |
| [Screen Content for Threats](actions/screen-content-for-threats.md) | `POST /guard` | [docs](https://docs.lakera.ai/api-reference/lakera-api/guard/screen-content) |
