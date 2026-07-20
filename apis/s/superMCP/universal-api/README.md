# <img src="https://images.mindcloud.co/apps/icons/favicon-mcp-supermetrics-com-48x48_1777646854027.png" alt="SuperMCP logo" width="28" height="28"> SuperMCP: Universal API

Query live marketing, advertising, analytics, ecommerce, and CRM data from Supermetrics through SuperMCP.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/superMCP/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://supermetrics.com
- **Vendor API docs:** https://mcp.supermetrics.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Discover Accounts](actions/discover-accounts.md) | GET |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Update Campaign](actions/update-campaign.md) | PUT |  |

### Campaign Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Resources](actions/get-campaign-resources.md) | GET |  |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Discover Data Sources](actions/discover-data-sources.md) | GET |  |

### Date Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Today](actions/get-today.md) | GET |  |

### Documentation

| Action | Method | Description |
| --- | --- | --- |
| [Get MCP Server Documentation](actions/get-mcp-server-documentation.md) | GET |  |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Discover Fields](actions/discover-fields.md) | GET |  |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET |  |

### Hub Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Supermetrics Hub Resource](actions/get-supermetrics-hub-resource.md) | GET |  |

### Marketing Data Query

| Action | Method | Description |
| --- | --- | --- |
| [Query Marketing Data](actions/query-marketing-data.md) | GET |  |

### Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Query Results](actions/get-async-query-results.md) | GET |  |

### Support Request

| Action | Method | Description |
| --- | --- | --- |
| [Contact Supermetrics](actions/contact-supermetrics.md) | POST |  |

### User Info

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET |  |

