# SuperMCP: Native API Reference

A consolidated summary of SuperMCP's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://mcp.supermetrics.com/
- **API base URL:** `https://mcp.supermetrics.com`

## Authentication

### API Key

Authenticate with a Supermetrics API key using Bearer token authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mcp.supermetrics.com/)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Contact Supermetrics](actions/contact-supermetrics.md) | `POST /mcp/contact_supermetrics` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Create Campaign](actions/create-campaign.md) | `POST /mcp/campaign_create` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Discover Accounts](actions/discover-accounts.md) | `POST /mcp/accounts_discovery` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Discover Data Sources](actions/discover-data-sources.md) | `POST /mcp/data_source_discovery` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Discover Fields](actions/discover-fields.md) | `POST /mcp/field_discovery` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Get Async Query Results](actions/get-async-query-results.md) | `POST /mcp/get_async_query_results` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Get Campaign Resources](actions/get-campaign-resources.md) | `POST /mcp/campaign_and_resource_get` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Get MCP Server Documentation](actions/get-mcp-server-documentation.md) | `GET /mcp/resources/docs` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Get Supermetrics Hub Resource](actions/get-supermetrics-hub-resource.md) | `GET /mcp/resources/hub` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Get Today](actions/get-today.md) | `POST /mcp/get_today` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Get User Info](actions/get-user-info.md) | `POST /mcp/user_info` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://mcp.supermetrics.com/) |
| [Query Marketing Data](actions/query-marketing-data.md) | `POST /mcp/data_query` | [docs](https://mcp.supermetrics.com/openapi.json) |
| [Update Campaign](actions/update-campaign.md) | `POST /mcp/campaign_update` | [docs](https://mcp.supermetrics.com/openapi.json) |
