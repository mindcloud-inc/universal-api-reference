# GSA Public Comment: Universal API

Query federal regulatory dockets, documents, and public comments from Regulations.gov.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gSAPublicComment/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.regulations.gov
- **Vendor API docs:** https://open.gsa.gov/api/regulationsgov/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agency Categories](actions/list-agency-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-agency-categories?connectionId=$CONNECTION_ID&acronym=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Agency Category

| Action | Method | Description |
| --- | --- | --- |
| [List Agency Categories](actions/list-agency-categories.md) | GET | Retrieves agency categories for an acronym from GSA Public Comment. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a specific comment from GSA Public Comment. |
| [List Comments](actions/list-comments.md) | GET | Retrieves a list of comments from GSA Public Comment. |

### Docket

| Action | Method | Description |
| --- | --- | --- |
| [Get Docket](actions/get-docket.md) | GET | Retrieves a specific docket from GSA Public Comment. |
| [List Dockets](actions/list-dockets.md) | GET | Retrieves a list of dockets from GSA Public Comment. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a specific document from GSA Public Comment. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from GSA Public Comment. |

