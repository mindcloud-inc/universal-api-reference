# Productify.ai: Native API Reference

A consolidated summary of Productify.ai's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.productify.ai/docs/
- **OpenAPI specification:** https://api.productify.ai/swagger/v1/swagger.json
- **API base URL:** `https://api.productify.ai`

## Authentication

### API Key

Authenticate requests with a Productify.ai workspace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ApiKey: <apiKey>
```

[Official authentication documentation](https://api.productify.ai/swagger/v1/swagger.json)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Health](actions/check-health.md) | `GET /health` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Create Digitisation Batch](actions/create-digitisation-batch.md) | `POST /Batch/Extract` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Create Ecommerce Batch](actions/create-ecommerce-batch.md) | `POST /Batch/Generate/Ecommerce` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Create Generate Batch](actions/create-generate-batch.md) | `POST /Batch/Generate` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Create Text Transform Batch](actions/create-text-transform-batch.md) | `POST /Batch/Transform` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /Account/Balance` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Batch Status](actions/get-batch-status.md) | `GET /Batch/Status` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Digitisation Batch Results](actions/get-digitisation-batch-results.md) | `POST /Result/Extract` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Digitisation Batch Results With GET](actions/get-digitisation-batch-results-with-get.md) | `GET /Result/Extract` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Ecommerce Batch Results](actions/get-ecommerce-batch-results.md) | `POST /Result/Generate/Ecommerce` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Generate Batch Results](actions/get-generate-batch-results.md) | `POST /Result/Generate` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Generate Batch Results With GET](actions/get-generate-batch-results-with-get.md) | `GET /Result/Generate` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Text Transform Batch Results](actions/get-text-transform-batch-results.md) | `POST /Result/Transform` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Text Transform Batch Results With GET](actions/get-text-transform-batch-results-with-get.md) | `GET /Result/Transform` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Get Workspace Details](actions/get-workspace-details.md) | `GET /workspace/detail` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [List Bonus Tiers](actions/list-bonus-tiers.md) | `GET /pricing/bonus-tiers` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [List Operation Costs](actions/list-operation-costs.md) | `GET /pricing/operation-costs` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [List Product Categories](actions/list-product-categories.md) | `GET /categories` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [List Supported Languages](actions/list-supported-languages.md) | `GET /languages` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [List Taxonomies](actions/list-taxonomies.md) | `GET /taxonomies` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Perform Digitisation Extract](actions/perform-digitisation-extract.md) | `POST /Single/Extract` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Perform Ecommerce Generate](actions/perform-ecommerce-generate.md) | `POST /Single/Generate/Ecommerce` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Perform Generate](actions/perform-generate.md) | `POST /Single/Generate` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Perform Text Transform](actions/perform-text-transform.md) | `POST /Single/Transform` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
| [Run System Test](actions/run-system-test.md) | `GET /Test` | [docs](https://api.productify.ai/swagger/v1/swagger.json) |
