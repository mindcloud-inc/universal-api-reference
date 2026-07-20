# <img src="https://images.mindcloud.co/apps/icons/glasp_1774987668325.png" alt="Glasp logo" width="28" height="28"> Glasp: Universal API

Collect, organize, and share highlights and notes from the web and PDFs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/glasp/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://glasp.co/
- **Vendor API docs:** https://glasp.co/docs/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Highlights](actions/export-highlights.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/glasp/latest/actions/export-highlights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Highlights](actions/create-highlights.md) | POST | Creates new highlights in your Glasp account. |
| [Delete Highlight](actions/delete-highlight.md) | DELETE | Deletes a Glasp highlight or all highlights in a document. |
| [Export Highlights](actions/export-highlights.md) | GET | Retrieves your Glasp highlights with optional filtering and pagination. |
| [Update Highlight](actions/update-highlight.md) | PUT | Updates an existing highlight in Glasp. |

