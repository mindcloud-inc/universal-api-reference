# <img src="https://images.mindcloud.co/apps/icons/c82b7899af218f370ce295e856e10a70_1775230475886.png" alt="Zoho Sign logo" width="28" height="28"> Zoho Sign: Universal API

Send, sign, and manage business documents and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoSign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/sign/
- **Vendor API docs:** https://www.zoho.com/sign/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Correct Document](actions/correct-document.md) | PUT | Marks a document for correction in Zoho Sign. |
| [Create Document](actions/create-document.md) | POST | Creates a document in Zoho Sign. |
| [Download Document PDF](actions/download-document-pdf.md) | GET | Downloads a document PDF from Zoho Sign. |
| [Download Particular PDF File](actions/download-particular-pdf-file.md) | GET | Downloads a particular PDF file from Zoho Sign. |
| [Get Document Details](actions/get-document-details.md) | GET | Retrieves document details from Zoho Sign. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Zoho Sign. |
| [Submit Document](actions/submit-document.md) | PUT | Submits a document for signature in Zoho Sign. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Zoho Sign. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Type](actions/create-document-type.md) | POST | Creates a document type in Zoho Sign. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Zoho Sign. |
| [Extend Document Expiry](actions/extend-document-expiry.md) | PUT | Extends document expiry in Zoho Sign. |
| [Get Document Form Data](actions/get-document-form-data.md) | GET | Retrieves document form data from Zoho Sign. |
| [List Document Types](actions/list-document-types.md) | GET | Retrieves document types from Zoho Sign. |
| [List Field Types](actions/list-field-types.md) | GET | Retrieves field types from Zoho Sign. |
| [Recall Document](actions/recall-document.md) | PUT | Recalls a document in Zoho Sign. |
| [Remind Recipient](actions/remind-recipient.md) | PUT | Sends a reminder to a recipient in Zoho Sign. |
| [Send Document Using Template](actions/send-document-using-template.md) | POST | Creates a document from a template in Zoho Sign. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in Zoho Sign. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Zoho Sign. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in Zoho Sign. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from Zoho Sign. |
| [Get Template Details](actions/get-template-details.md) | GET | Retrieves template details from Zoho Sign. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Zoho Sign. |

