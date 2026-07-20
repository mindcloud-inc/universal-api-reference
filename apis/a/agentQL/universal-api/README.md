# <img src="https://images.mindcloud.co/apps/icons/agent-ql_1774617676341.png" alt="AgentQL logo" width="28" height="28"> AgentQL: Universal API

Extract web and document data, and run remote browser sessions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agentQL/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.agentql.com
- **Vendor API docs:** https://docs.agentql.com/rest-api/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Browser Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Remote Browser Session](actions/create-remote-browser-session.md) | POST | Creates a remote browser session with CDP access in AgentQL. |

### Document Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Query Document](actions/query-document.md) | GET | Queries structured data from documents and images with AgentQL. |

### Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Query Data](actions/query-data.md) | GET | Queries structured data from web pages with AgentQL. |

### Session Usage

| Action | Method | Description |
| --- | --- | --- |
| [List Session Usage](actions/list-session-usage.md) | GET | Retrieves Tetra browser session usage from AgentQL. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves API key usage and subscription details from AgentQL. |

