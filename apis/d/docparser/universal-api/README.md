# <img src="https://images.mindcloud.co/apps/icons/id-zapb6wu-o-1773347381172_1773347400999.png" alt="Docparser logo" width="28" height="28"> Docparser: Universal API

Extract structured data from PDFs, images, and business documents with Docparser parsers and the Docparser API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docparser/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docparser.com/
- **Vendor API docs:** https://docparser.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Data Of Multiple Documents](actions/get-data-of-multiple-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-data-of-multiple-documents?connectionId=$CONNECTION_ID&parserId=tiumtyrcddpn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Api Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Checks Docparser API authentication. |

### Document Parser

| Action | Method | Description |
| --- | --- | --- |
| [List Document Parsers](actions/list-document-parsers.md) | GET | Retrieves document parsers from Docparser. |

### Document Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Status](actions/get-document-status.md) | GET | Retrieves status details for a Docparser document. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Document From URL](actions/fetch-document-from-url.md) | POST | Fetches a document from a URL into a Docparser parser. |
| [Fetch Document From URL With Remote ID](actions/fetch-document-from-url-with-remote-id.md) | POST | Fetches a document from a URL into a Docparser parser and assigns a remote ID. |
| [Re-Integrate Data](actions/re-integrate-data.md) | PUT | Schedules Docparser documents for re-integration. |
| [Re-Parse Data](actions/re-parse-data.md) | PUT | Schedules Docparser documents for re-parsing. |
| [Upload Document By Content](actions/upload-document-by-content.md) | POST | Uploads document content to a Docparser parser. |
| [Upload Document By Content With Remote ID](actions/upload-document-by-content-with-remote-id.md) | POST | Uploads document content to a Docparser parser and assigns a remote ID. |
| [Upload Document From Local Path](actions/upload-document-from-local-path.md) | POST | Uploads a local document to a Docparser parser. |
| [Upload Document From Local Path With Remote ID](actions/upload-document-from-local-path-with-remote-id.md) | POST | Uploads a local document to a Docparser parser and assigns a remote ID. |

### Parsed Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Of Multiple Documents](actions/get-data-of-multiple-documents.md) | GET | Retrieves parsed data for multiple Docparser documents. |
| [Get Data Of Multiple Documents By Remote ID](actions/get-data-of-multiple-documents-by-remote-id.md) | GET | Retrieves parsed data for Docparser documents by remote ID. |
| [Get Data Of One Document](actions/get-data-of-one-document.md) | GET | Retrieves parsed data for one Docparser document. |
| [Get Data Of One Document Including Children](actions/get-data-of-one-document-including-children.md) | GET | Retrieves parsed data for one Docparser document including child parser results. |
| [Get Flat Data Of Multiple Documents](actions/get-flat-data-of-multiple-documents.md) | GET | Retrieves flat parsed data for multiple Docparser documents. |
| [Get Flat Data Of One Document](actions/get-flat-data-of-one-document.md) | GET | Retrieves flat parsed data for one Docparser document. |
| [Get Sorted Data Of Multiple Documents](actions/get-sorted-data-of-multiple-documents.md) | GET | Retrieves sorted parsed data for multiple Docparser documents. |

### Parser Model Layout

| Action | Method | Description |
| --- | --- | --- |
| [List Parser Model Layouts](actions/list-parser-model-layouts.md) | GET | Retrieves parser model layouts from Docparser. |

