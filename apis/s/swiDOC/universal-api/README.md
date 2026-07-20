# <img src="https://images.mindcloud.co/apps/icons/favicon-api-docs-swidoc-ch-48x48_1777046030874.png" alt="swiDOC logo" width="28" height="28"> swiDOC: Universal API

swiDOC provides a secure, legally compliant document archiving API for storing, retrieving, and managing archived document metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swiDOC/latest
- **Category:** Content & Files / Storage
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.swidoc.ch
- **Vendor API docs:** https://api.docs.swidoc.ch/swagger.yml

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Document Metadata](actions/get-document-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/get-document-metadata?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Archive Document](actions/archive-document.md) | POST | Archives a document in swiDOC. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from swiDOC by document ID. |

### Document Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Metadata](actions/get-document-metadata.md) | GET | Retrieves document metadata from swiDOC by document ID. |
| [Update Document Metadata](actions/update-document-metadata.md) | PUT | Updates document metadata in swiDOC by document ID. |

