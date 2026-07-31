# Agify: Native API Reference

A consolidated summary of Agify's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://agify.io/documentation/api/reference
- **API base URL:** `https://api.agify.io`

## Authentication

### API key

Agify API key passed as the shared apikey query parameter.

### Credentials

- **Agify API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://agify.io/documentation/api/reference)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Predict Age](actions/predict-age.md) | `GET /` | [docs](https://agify.io/documentation/api/reference) |
| [Predict Ages](actions/predict-ages.md) | `GET /` | [docs](https://agify.io/documentation/api/reference) |
