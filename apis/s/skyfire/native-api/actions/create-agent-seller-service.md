# Create Agent Seller Service with Skyfire

Creates a new agent seller service in Skyfire.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/seller-services`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Create Agent Seller Service](https://docs.skyfire.xyz/reference/create-agents-service-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Internal and public-facing service name. |
| `description` | body | `string` | no | What your service does and how buyers use it. |
| `serviceType` | body | `string` | no | Choose from API, Web Page, or MCP Server. |
| `serviceUrl` | body | `string` | no | Provide the OpenAPI spec, public website URL, or MCP server endpoint depending on type. |
| `price` | body | `string` | no | Price of the service in USD. |
| `priceModel` | body | `string` | no | Per-use, per-MB, or subscription pricing model. |
| `termsOfServiceUrl` | body | `string` | no | Link to your legal terms or usage policy. |
