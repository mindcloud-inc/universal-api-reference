# <img src="https://images.mindcloud.co/apps/icons/youcom_1774984884072.png" alt="You.com logo" width="28" height="28"> You.com: Universal API

Search the web, extract content, and run AI agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/youcom/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://you.com
- **Vendor API docs:** https://docs.you.com/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search](actions/search.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Search Images](actions/search-images.md) | GET | Retrieves image search results from You.com. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Ask Advanced Agent](actions/ask-advanced-agent.md) | GET | Retrieves an advanced agent response from You.com. |
| [Ask Express Agent](actions/ask-express-agent.md) | GET | Retrieves an express agent response from You.com. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Contents](actions/get-contents.md) | GET | Retrieves page contents from You.com. |
| [Get Live News](actions/get-live-news.md) | GET | Retrieves live news results from You.com. |
| [Search](actions/search.md) | GET | Retrieves search results from You.com. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Research](actions/research.md) | GET | Retrieves a research report from You.com. |

