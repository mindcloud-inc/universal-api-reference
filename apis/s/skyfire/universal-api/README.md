# <img src="https://images.mindcloud.co/apps/icons/skyfire_1776961199129.png" alt="Skyfire logo" width="28" height="28"> Skyfire: Universal API

Create, verify, and charge AI identity and payment tokens

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/skyfire/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://skyfire.xyz
- **Vendor API docs:** https://docs.skyfire.xyz/docs/developer-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Services](actions/list-services.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Charge Token](actions/charge-token.md) | POST | Creates a new token charge in Skyfire. |

### Enterprise User

| Action | Method | Description |
| --- | --- | --- |
| [Create Enterprise User](actions/create-enterprise-user.md) | POST | Creates a new enterprise user in Skyfire. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Activate Agent Seller Service](actions/activate-agent-seller-service.md) | PUT | Activates an existing agent seller service in Skyfire. |
| [Create Agent Seller Service](actions/create-agent-seller-service.md) | POST | Creates a new agent seller service in Skyfire. |
| [Deactivate Agent Seller Service](actions/deactivate-agent-seller-service.md) | PUT | Deactivates an existing agent seller service in Skyfire. |
| [Get Agent Seller Service](actions/get-agent-seller-service.md) | GET | Retrieves an agent seller service from Skyfire. |
| [Get Agent Seller Services](actions/get-agent-seller-services.md) | GET | Retrieves an agent's seller services from Skyfire. |
| [Get Service](actions/get-service.md) | GET | Retrieves a service from Skyfire. |
| [Get Services by Agent](actions/get-services-by-agent.md) | GET | Retrieves services for an agent in Skyfire. |
| [Get Services by Tags](actions/get-services-by-tags.md) | GET | Retrieves Skyfire services by tags. |
| [List Services](actions/list-services.md) | GET | Retrieves services from Skyfire. |
| [Update Agent Seller Service](actions/update-agent-seller-service.md) | PUT | Updates an existing agent seller service in Skyfire. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get All Service Tags](actions/get-all-service-tags.md) | GET | Retrieves all service tags from Skyfire. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Token](actions/create-token.md) | POST | Creates a new token in Skyfire. |
| [Introspect Token](actions/introspect-token.md) | GET | Retrieves token details from Skyfire. |

### Token Charge

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Charges](actions/get-token-charges.md) | GET | Retrieves token charges from Skyfire. |

### Wallet Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Wallet Balance](actions/get-agent-wallet-balance.md) | GET | Retrieves an agent wallet balance from Skyfire. |

