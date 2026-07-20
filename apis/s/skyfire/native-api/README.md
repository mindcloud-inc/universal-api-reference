# Skyfire: Native API Reference

A consolidated summary of Skyfire's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.skyfire.xyz/docs/developer-documentation
- **API base URL:** `https://api.skyfire.xyz/api/v1`

## Authentication

### API Key

Authenticate Skyfire API requests with an agent API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.skyfire.xyz/reference/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Agent Seller Service](actions/activate-agent-seller-service.md) | `POST /agents/seller-services/:sellerServiceId/activate` | [docs](https://docs.skyfire.xyz/reference/create-agents-service) |
| [Charge Token](actions/charge-token.md) | `POST /tokens/charge` | [docs](https://docs.skyfire.xyz/reference/charge-token) |
| [Create Agent Seller Service](actions/create-agent-seller-service.md) | `POST /agents/seller-services` | [docs](https://docs.skyfire.xyz/reference/create-agents-service-1) |
| [Create Enterprise User](actions/create-enterprise-user.md) | `POST /organizations/users` | [docs](https://docs.skyfire.xyz/reference/create-enterprise-user) |
| [Create Token](actions/create-token.md) | `POST /tokens` | [docs](https://docs.skyfire.xyz/reference/create-token) |
| [Deactivate Agent Seller Service](actions/deactivate-agent-seller-service.md) | `POST /agents/seller-services/:sellerServiceId/deactivate` | [docs](https://docs.skyfire.xyz/reference/deactivate-agents-service) |
| [Get Agent Seller Service](actions/get-agent-seller-service.md) | `GET /agents/seller-services/:sellerServiceId` | [docs](https://docs.skyfire.xyz/reference/get-agents-service) |
| [Get Agent Seller Services](actions/get-agent-seller-services.md) | `GET /agents/seller-services` | [docs](https://docs.skyfire.xyz/reference/get-agents-seller-services-all) |
| [Get Agent Wallet Balance](actions/get-agent-wallet-balance.md) | `GET /agents/balance` | [docs](https://docs.skyfire.xyz/reference/get-agents-wallet-balance) |
| [Get All Service Tags](actions/get-all-service-tags.md) | `GET /directory/tags` | [docs](https://docs.skyfire.xyz/reference/get-all-service-tags) |
| [Get Service](actions/get-service.md) | `GET /directory/services/:serviceId` | [docs](https://docs.skyfire.xyz/reference/get-service) |
| [Get Services by Agent](actions/get-services-by-agent.md) | `GET /directory/agents/:agentId/services` | [docs](https://docs.skyfire.xyz/reference/get-services-by-agent) |
| [Get Services by Tags](actions/get-services-by-tags.md) | `GET /directory/services/search` | [docs](https://docs.skyfire.xyz/reference/get-services-by-tags) |
| [Get Token Charges](actions/get-token-charges.md) | `GET /tokens/:tokenId/charges` | [docs](https://docs.skyfire.xyz/reference/get-token-charges) |
| [Introspect Token](actions/introspect-token.md) | `POST /tokens/introspect` | [docs](https://docs.skyfire.xyz/reference/introspect-token) |
| [List Services](actions/list-services.md) | `GET /directory/services` | [docs](https://docs.skyfire.xyz/reference/get-all-services) |
| [Update Agent Seller Service](actions/update-agent-seller-service.md) | `PATCH /agents/seller-services/:sellerServiceId` | [docs](https://docs.skyfire.xyz/reference/update-agents-service) |
