# <img src="https://images.mindcloud.co/apps/icons/google-docs-default_1779718939326.png" alt="Google Docs logo" width="28" height="28"> Google Docs: Universal API

Create documents, collaborate in real time, review feedback, and refine content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleDocs/latest
- **Category:** Content & Files / Storage
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docs.google.com
- **Vendor API docs:** https://developers.google.com/workspace/docs/api/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Blank Document](actions/create-blank-document.md) | POST | Creates a new blank document in Google Docs. |
| [Delete Document](actions/delete-document.md) | DELETE | Permanently deletes a Google Docs document from Google Drive. |
| [Get Document](actions/get-document.md) | GET | Retrieves a Google Docs document by ID. |
| [Insert Text](actions/insert-text.md) | PUT | Inserts text into a Google Docs document. |
| [List Documents](actions/list-documents.md) | GET | Finds Google Docs and Word documents in Google Drive. |
| [Replace All Text](actions/replace-all-text.md) | PUT | Replaces matching text in a Google Docs document. |

