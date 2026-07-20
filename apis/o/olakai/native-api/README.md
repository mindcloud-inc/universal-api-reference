# Olakai: Native API Reference

A consolidated summary of Olakai's API configuration, with links to official documentation.

- **Official docs:** https://app.olakai.ai/docs/olakai/api-sdk-rest-api
- **API base URL:** `https://app.olakai.ai/api/monitoring`

## Authentication

### API Key

Connect to Olakai with the recommended x-api-key authentication method documented for the monitoring API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://app.olakai.ai/docs/olakai/api-sdk-rest-api)

## API conventions

Responses from this API use JSON.
