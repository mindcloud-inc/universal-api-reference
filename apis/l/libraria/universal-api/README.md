# <img src="https://images.mindcloud.co/apps/icons/libraria_1775491728362.png" alt="Libraria logo" width="28" height="28"> Libraria: Universal API

Query libraries, manage documents, and embed AI assistants

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/libraria/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://libraria.ai
- **Vendor API docs:** https://docs.libraria.ai/api-reference/home

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Document](actions/get-document.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraria/latest/actions/get-document?connectionId=$CONNECTION_ID&libraryId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Add Document](actions/add-document.md) | POST | Add a new document to your library via scraping or raw text. |
| [Delete Document](actions/delete-document.md) | DELETE | Delete a document from a library. |
| [Get Document](actions/get-document.md) | GET | Get a document from a library. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Create Query](actions/create-query.md) | POST | Make queries to a specific chatbot or library. |
| [Create Query (Legacy)](actions/create-query-legacy.md) | POST | Given a query and an optional conversation ID, get a response from your library. |

