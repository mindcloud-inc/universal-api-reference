# <img src="https://images.mindcloud.co/apps/icons/images-28_1774901221833.png" alt="Docsumo logo" width="28" height="28"> Docsumo: Universal API

Process, classify, review, and extract structured data from documents and cases with Docsumo OCR and workflow APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docsumo/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docsumo.com
- **Vendor API docs:** https://support.docsumo.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User And Document Types](actions/get-user-and-document-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/get-user-and-document-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [Delete Cases](actions/delete-cases.md) | DELETE | Deletes existing cases from a Docsumo case type. |
| [Get Case Overview](actions/get-case-overview.md) | GET | Retrieves overview details for a Docsumo case. |
| [Get Case Type Details](actions/get-case-type-details.md) | GET | Retrieves configuration details for a Docsumo case type. |
| [List Cases](actions/list-cases.md) | GET | Retrieves cases for a Docsumo case type. |
| [Run Case Workflow](actions/run-case-workflow.md) | PUT | Triggers a workflow for a Docsumo case. |
| [Update Case](actions/update-case.md) | PUT | Updates an existing case in Docsumo. |
| [Upload Case](actions/upload-case.md) | POST | Creates or updates a Docsumo case and uploads files. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Add Files In Folder](actions/add-files-in-folder.md) | POST | Uploads a document into a specific Docsumo folder. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Docsumo. |
| [Get Bank Statement Analytics](actions/get-bank-statement-analytics.md) | GET | Retrieves bank statement analytics for a Docsumo document. |
| [Get Document Details](actions/get-document-details.md) | GET | Retrieves detailed metadata for a document in Docsumo. |
| [Get Document Review URL](actions/get-document-review-url.md) | GET | Retrieves a signed document review URL from Docsumo. |
| [Get Documents Summary](actions/get-documents-summary.md) | GET | Retrieves document counts by type and status in Docsumo. |
| [Get Extracted Data](actions/get-extracted-data.md) | GET | Retrieves simplified extracted data for a Docsumo document. |
| [Get Split File URLs](actions/get-split-file-urls.md) | GET | Retrieves split-document file URLs from Docsumo. |
| [Get Split Info](actions/get-split-info.md) | GET | Retrieves split-document metadata and file options from Docsumo. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Docsumo with filtering and sorting. |
| [Move Documents Between Folders](actions/move-documents-between-folders.md) | PUT | Moves documents between folders in Docsumo. |
| [Set Document Review Status](actions/set-document-review-status.md) | PUT | Updates a document's review status in Docsumo. |
| [Update Extracted Field](actions/update-extracted-field.md) | PUT | Updates an extracted field value in a Docsumo document. |
| [Upload File](actions/upload-file.md) | POST | Uploads a document file to Docsumo. |
| [Upload File From URL Or Base64](actions/upload-file-from-url-or-base64.md) | POST | Uploads a document to Docsumo from a URL or Base64. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Docsumo. |
| [Get Folder Review URL](actions/get-folder-review-url.md) | GET | Retrieves a secure folder review URL from Docsumo. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Run MCA Analysis](actions/run-mca-analysis.md) | GET | Retrieves monthly account summary analysis from Docsumo bank statements. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Table](actions/add-table.md) | POST | Creates a database table in Docsumo. |
| [Add Table Row](actions/add-table-row.md) | POST | Adds an empty row to a Docsumo database table. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes one or more Docsumo database tables. |
| [Get Table Data](actions/get-table-data.md) | GET | Retrieves all rows from a Docsumo database table. |
| [Update Table Cell](actions/update-table-cell.md) | PUT | Updates a single cell in a Docsumo database table. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User And Document Types](actions/get-user-and-document-types.md) | GET | Retrieves your Docsumo user details and active document types. |
| [List Agents](actions/list-agents.md) | GET | Retrieves Docsumo agents by case or document type. |
| [List Enabled Document Types](actions/list-enabled-document-types.md) | GET | Retrieves enabled document types from Docsumo. |

