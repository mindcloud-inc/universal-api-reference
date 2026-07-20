# Tavus: Native API Reference

A consolidated summary of Tavus's API configuration, with links to official documentation.

- **Official docs:** https://docs.tavus.io/api-reference/overview
- **OpenAPI specification:** https://docs.tavus.io/openapi.yaml
- **API base URL:** `https://tavusapi.com/v2`

## Authentication

### API Key

Authenticate Tavus API requests with a Tavus Developer Portal API key.

### Credentials

- **Tavus API key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.tavus.io/api-reference/authentication)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
