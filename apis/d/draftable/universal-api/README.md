# <img src="https://images.mindcloud.co/apps/icons/draftable-icon_1775831074390.png" alt="Draftable logo" width="28" height="28"> Draftable: Universal API

Compare documents and export review-ready PDFs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/draftable/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://draftable.com
- **Vendor API docs:** https://api.draftable.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Comparisons](actions/list-comparisons.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/list-comparisons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Comparison](actions/create-comparison.md) | POST | Creates a document comparison in Draftable. |
| [Delete Comparison](actions/delete-comparison.md) | DELETE | Deletes a document comparison from Draftable. |
| [Get Comparison](actions/get-comparison.md) | GET | Retrieves a document comparison from Draftable. |
| [List Comparisons](actions/list-comparisons.md) | GET | Retrieves your document comparisons from Draftable. |

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Export Comparison as PDF](actions/export-comparison-as-pdf.md) | POST | Creates a PDF export job in Draftable. |
| [Get Export](actions/get-export.md) | GET | Retrieves a comparison export job from Draftable. |

