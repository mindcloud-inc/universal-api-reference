# Dataway: Native API Reference

A consolidated summary of Dataway's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/421216/UV5Ukz4U
- **API base URL:** `https://datawayapp.com/vendor`

## Authentication

### Dataway Vendor Keys

Custom auth for Dataway vendor API using API public key and API private key.

### Credentials

- **API Public Key:** `apiPublicKey` · required · Dataway tenant public key.
- **API Private Key:** `apiPrivateKey` · required · Dataway tenant private key.

[Official authentication documentation](https://documenter.getpostman.com/view/421216/UV5Ukz4U)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | `POST /balance` | [docs](https://documenter.getpostman.com/view/421216/UV5Ukz4U) |
| [List Service Categories](actions/list-service-categories.md) | `GET /get-service-categories` | [docs](https://documenter.getpostman.com/view/421216/UV5Ukz4U) |
| [List Service Variations](actions/list-service-variations.md) | `GET /get-service-variations` | [docs](https://documenter.getpostman.com/view/421216/UV5Ukz4U) |
| [List Services](actions/list-services.md) | `GET /get-services` | [docs](https://documenter.getpostman.com/view/421216/UV5Ukz4U) |
| [Query Transaction](actions/query-transaction.md) | `POST /query-transaction` | [docs](https://documenter.getpostman.com/view/421216/UV5Ukz4U) |
| [Validate Biller](actions/validate-biller.md) | `POST /validate-biller` | [docs](https://documenter.getpostman.com/view/421216/UV5Ukz4U) |
| [Vend Service](actions/vend-service.md) | `POST /vend` | [docs](https://documenter.getpostman.com/view/421216/UV5Ukz4U) |
