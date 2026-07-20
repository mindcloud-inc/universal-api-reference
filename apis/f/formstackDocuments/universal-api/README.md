# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-03-12-as-21_1773361515402.png" alt="Formstack Documents logo" width="28" height="28"> Formstack Documents: Universal API

Formstack Documents: Create, merge, and deliver automated documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formstackDocuments/latest
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.formstack.com/products/documents
- **Vendor API docs:** https://www.webmerge.me/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Data Route

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Route](actions/create-data-route.md) | POST | Creates a new data route in Formstack Documents. |
| [Create Data Route Delivery](actions/create-data-route-delivery.md) | POST | Creates a data route delivery in Formstack Documents. |
| [Delete Data Route](actions/delete-data-route.md) | DELETE | Deletes an existing data route from Formstack Documents. |
| [Get Data Route](actions/get-data-route.md) | GET | Retrieves data route details from Formstack Documents. |
| [List Data Route Deliveries](actions/list-data-route-deliveries.md) | GET | Retrieves data route deliveries from Formstack Documents. |
| [List Data Route Fields](actions/list-data-route-fields.md) | GET | Retrieves data route fields from Formstack Documents. |
| [List Data Route Rules](actions/list-data-route-rules.md) | GET | Retrieves data route rules from Formstack Documents. |
| [List Data Routes](actions/list-data-routes.md) | GET | Retrieves data routes from Formstack Documents. |
| [Merge Data Route](actions/merge-data-route.md) | POST | Merges data through a data route in Formstack Documents. |
| [Update Data Route](actions/update-data-route.md) | PUT | Updates an existing data route in Formstack Documents. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Copy Document](actions/copy-document.md) | POST | Creates a copy of a document in Formstack Documents. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Formstack Documents. |
| [Create Document Delivery](actions/create-document-delivery.md) | POST | Creates a document delivery in Formstack Documents. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Formstack Documents. |
| [Get Document](actions/get-document.md) | GET | Retrieves document details from Formstack Documents. |
| [Get Document File](actions/get-document-file.md) | GET | Retrieves a document file from Formstack Documents. |
| [List Document Deliveries](actions/list-document-deliveries.md) | GET | Retrieves document deliveries from Formstack Documents. |
| [List Document Fields](actions/list-document-fields.md) | GET | Retrieves document fields from Formstack Documents. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from Formstack Documents. |
| [Merge Document](actions/merge-document.md) | POST | Merges data into a document in Formstack Documents. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Formstack Documents. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Combine Files](actions/combine-files.md) | POST | Combines files into one file in Formstack Documents. |
| [Compress PDF](actions/compress-pdf.md) | POST | Compresses a PDF file in Formstack Documents. |
| [Convert File to PDF](actions/convert-file-to-pdf.md) | POST | Converts a file to PDF in Formstack Documents. |
| [Encrypt PDF](actions/encrypt-pdf.md) | POST | Encrypts a PDF file in Formstack Documents. |
| [Split PDF](actions/split-pdf.md) | POST | Splits a PDF file in Formstack Documents. |

