# <img src="https://images.mindcloud.co/apps/icons/p-dfsplit-and-pdfmerge_1775755218763.png" alt="PDF Split and PDF Merge logo" width="28" height="28"> PDF Split and PDF Merge: Universal API

Split, merge, convert, and extract PDF and image files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFSplitAndPDFMerge/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pdfapihub.com
- **Vendor API docs:** https://pdfapihub.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFSplitAndPDFMerge/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET |  |

