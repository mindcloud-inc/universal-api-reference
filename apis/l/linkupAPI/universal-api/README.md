# <img src="https://images.mindcloud.co/apps/icons/linkup-api_1774878925426.png" alt="LinkupAPI logo" width="28" height="28"> LinkupAPI: Universal API

Search the web, fetch pages, and run research with Linkup

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkupAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.linkup.so
- **Vendor API docs:** https://docs.linkup.so/pages/documentation/get-started/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits Balance](actions/get-credits-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits Balance](actions/get-credits-balance.md) | GET | Retrieves your current credits balance from LinkupAPI. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Page](actions/fetch-page.md) | GET | Retrieves a single webpage by URL from LinkupAPI. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Research Task](actions/create-research-task.md) | POST | Creates a new research task in LinkupAPI. |
| [Get Research Task](actions/get-research-task.md) | GET | Retrieves research task details from LinkupAPI. |
| [List Research Tasks](actions/list-research-tasks.md) | GET | Retrieves a list of research tasks from LinkupAPI. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Generate Response](actions/generate-response.md) | GET | Generates an OpenAI-style response through LinkupAPI. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds web content in LinkupAPI by query. |

