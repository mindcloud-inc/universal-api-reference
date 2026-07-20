# Muna: Native API Reference

A consolidated summary of Muna's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.muna.ai/
- **API base URL:** `https://api.muna.ai`

## Authentication

### API Key

Use a Muna access key.

### Credentials

- **API Key:** `apiKey` · required
- **Access Key:** `accessKey` · required · Your Muna access key from the developer settings page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.muna.ai/security)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Prediction](actions/create-prediction.md) | `POST /v1/predictions` | [docs](https://docs.muna.ai/ref/predictions/create) |
| [Retrieve Predictor](actions/retrieve-predictor.md) | `GET /v1/predictors/{tag}` | [docs](https://docs.muna.ai/ref/predictors/retrieve) |
