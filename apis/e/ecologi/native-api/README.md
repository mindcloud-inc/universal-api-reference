# Ecologi: Native API Reference

A consolidated summary of Ecologi's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.ecologi.com/
- **API base URL:** `https://public.ecologi.com`

## Authentication

### API Key

Use an Ecologi API key from Settings > API. Purchase actions also require billing details on the Ecologi account before create requests will succeed.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.ecologi.com/api-automation-overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Total Habitat Restored](actions/get-total-habitat-restored.md) | `GET /users/:username/habitat-restoration` | [docs](https://docs.ecologi.com/docs/public-api-docs/3c74a892cdd4c-get-total-habitat-restored) |
| [Get Total Impact](actions/get-total-impact.md) | `GET /users/:username/impact` | [docs](https://docs.ecologi.com/docs/public-api-docs/0eb5caf374377-get-total-impact) |
| [Get Total Number of Trees](actions/get-total-number-of-trees.md) | `GET /users/:username/trees` | [docs](https://docs.ecologi.com/docs/public-api-docs/2531efb510c5b-get-total-number-of-trees) |
| [Get Total Tonnes of CO2e Avoided](actions/get-total-tonnes-of-co2e-avoided.md) | `GET /users/:username/carbon-offset` | [docs](https://docs.ecologi.com/docs/public-api-docs/6046ba6f68449-get-total-tonnes-of-co-e-avoided) |
| [Get Total Tonnes of CO2e Removed](actions/get-total-tonnes-of-co2e-removed.md) | `GET /users/:username/carbon-removal` | [docs](https://docs.ecologi.com/docs/public-api-docs/71d944cfdd8cd-get-total-tonnes-of-co-e-removed) |
| [Purchase Carbon Avoidance](actions/purchase-carbon-avoidance.md) | `POST /impact/carbon` | [docs](https://docs.ecologi.com/docs/public-api-docs/e07bbee7fa605-purchase-carbon-avoidance) |
| [Purchase Carbon Removals](actions/purchase-carbon-removals.md) | `POST /impact/carbon-removal` | [docs](https://docs.ecologi.com/docs/public-api-docs/f65cbeae299f9-purchase-carbon-removals) |
| [Purchase Habitat Restoration](actions/purchase-habitat-restoration.md) | `POST /impact/habitat-restoration` | [docs](https://docs.ecologi.com/docs/public-api-docs/4e33697efbfdf-purchase-habitat-restoration) |
| [Purchase Trees](actions/purchase-trees.md) | `POST /impact/trees` | [docs](https://docs.ecologi.com/docs/public-api-docs/004342d262f93-purchase-trees) |
