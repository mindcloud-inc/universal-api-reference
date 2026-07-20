# <img src="https://images.mindcloud.co/apps/icons/signing-hub_1774978819678.png" alt="SigningHub logo" width="28" height="28"> SigningHub: Universal API

Send, review, approve, and sign documents digitally

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signingHub/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.signinghub.com/
- **Vendor API docs:** https://manuals.nsignhub.com/latest/Api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from SigningHub. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments from SigningHub. |
| [Upload Attachment](actions/upload-attachment.md) | POST | Uploads an attachment to SigningHub. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attachment](actions/delete-attachment.md) | DELETE | Deletes an attachment from SigningHub. |
| [Download Attachment](actions/download-attachment.md) | GET | Downloads an attachment from SigningHub. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Digital Signature Field](actions/add-digital-signature-field.md) | POST | Adds a digital signature field in SigningHub. |
| [Add Text Box Field](actions/add-text-box-field.md) | POST | Adds a text box field in SigningHub. |
| [Get Document Details](actions/get-document-details.md) | GET | Retrieves document details from SigningHub. |
| [Get Document Verification](actions/get-document-verification.md) | GET | Retrieves document verification details from SigningHub. |
| [Upload Document](actions/upload-document.md) | POST | Uploads a document to SigningHub. |
| [Upload Document Base64](actions/upload-document-base64.md) | POST | Uploads a base64 document to SigningHub. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Change Document Order](actions/change-document-order.md) | PUT | Updates document order in SigningHub. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from SigningHub. |
| [Download Document](actions/download-document.md) | GET | Downloads a document from SigningHub. |
| [Download Package](actions/download-package.md) | GET | Downloads a package from SigningHub. |
| [Fill Form Fields](actions/fill-form-fields.md) | PUT | Fills form fields in SigningHub. |
| [Merge All Documents](actions/merge-all-documents.md) | POST | Merges all documents in a package in SigningHub. |
| [Rename Document](actions/rename-document.md) | PUT | Renames a document in SigningHub. |
| [Sign Document](actions/sign-document.md) | POST | Signs a document in SigningHub. |
| [Update Document](actions/update-document.md) | PUT | Updates a document in SigningHub. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Document Fields](actions/list-document-fields.md) | GET | Retrieves document fields from SigningHub. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Sign Packages](actions/bulk-sign-packages.md) | POST | Signs packages in bulk in SigningHub. |
| [Delete Package](actions/delete-package.md) | DELETE | Deletes a package from SigningHub. |
| [Move Package To Folder](actions/move-package-to-folder.md) | PUT | Moves a package to a folder in SigningHub. |
| [Rename Package](actions/rename-package.md) | PUT | Renames a package in SigningHub. |
| [Validate Bulk Sign Packages](actions/validate-bulk-sign-packages.md) | POST | Validates packages for bulk signing in SigningHub. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Add Package](actions/add-package.md) | POST | Creates a package in SigningHub. |
| [Get Package Details](actions/get-package-details.md) | GET | Retrieves package details from SigningHub. |
| [Get Package Timeline](actions/get-package-timeline.md) | GET | Retrieves package timeline details from SigningHub. |
| [Get Package Verification](actions/get-package-verification.md) | GET | Retrieves package verification details from SigningHub. |
| [List Packages](actions/list-packages.md) | GET | Retrieves packages from SigningHub. |

### Signature Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature Settings](actions/get-signature-settings.md) | GET | Retrieves signature settings from SigningHub. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Send Reminder](actions/send-reminder.md) | POST | Sends a workflow reminder in SigningHub. |
| [Share Document Package](actions/share-document-package.md) | POST | Shares a document package in SigningHub. |
| [Start New Workflow From Existing Package](actions/start-new-workflow-from-existing-package.md) | POST | Creates a new workflow from an existing package in SigningHub. |

### Workflow User

| Action | Method | Description |
| --- | --- | --- |
| [Add Workflow Users](actions/add-workflow-users.md) | POST | Adds users to a workflow in SigningHub. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Details](actions/get-workflow-details.md) | GET | Retrieves workflow details from SigningHub. |
| [List Workflow Users](actions/list-workflow-users.md) | GET | Retrieves workflow users from SigningHub. |
| [Recall Document](actions/recall-document.md) | DELETE | Recalls a document workflow in SigningHub. |
| [Update Workflow User Permissions](actions/update-workflow-user-permissions.md) | PUT | Updates workflow user permissions in SigningHub. |

