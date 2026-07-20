# SigningHub: Native API Reference

A consolidated summary of SigningHub's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://manuals.nsignhub.com/latest/Api/
- **API base URL:** `https://api.signinghub.com`

## Authentication

### OAuth 2.0

### Credentials

- **Username:** `username` · optional · SigningHub email address for the target user account.
- **Client ID:** `clientId` · optional · Application name configured in SigningHub enterprise integration settings.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.signinghub.com/authenticate.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


Refresh expired access tokens with a POST request to https://api.signinghub.com/authenticate. A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.ascertia.com/signinghub-web/configurations/enterprise-configurations/integrate-third-party-applications/manage-third-party-integrations)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Digital Signature Field](actions/add-digital-signature-field.md) | `POST /v4/packages/:packageId/documents/:documentId/fields/signature` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Preparation/operation/V4_Signature_AddSignature) |
| [Add Package](actions/add-package.md) | `POST /v4/packages` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_AddPackage) |
| [Add Text Box Field](actions/add-text-box-field.md) | `POST /v4/packages/:packageId/documents/:documentId/fields/text` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Preparation/operation/V4_TextBox_AddTextBox) |
| [Add Workflow Users](actions/add-workflow-users.md) | `POST /v4/packages/:packageId/workflow/users` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Workflow_WorkflowAddUser) |
| [Bulk Sign Packages](actions/bulk-sign-packages.md) | `POST /v4/packages/SIGN` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Signing_BulkSignDocuments) |
| [Change Document Order](actions/change-document-order.md) | `PUT /v4/packages/:packageId/documents/:documentId/reorder` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UpdateDocumentOrder) |
| [Delete Attachment](actions/delete-attachment.md) | `DELETE /v4/packages/:packageId/documents/:documentId/attachments/:attachmentId` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_DeleteAttachment) |
| [Delete Document](actions/delete-document.md) | `DELETE /v4/packages/:packageId/documents/:documentId` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_DeleteDocument) |
| [Delete Package](actions/delete-package.md) | `DELETE /v4/packages/:packageId` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_DeletePackage) |
| [Download Attachment](actions/download-attachment.md) | `GET /v4/packages/:packageId/documents/:documentId/attachments/:attachment_id` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_DownloadAttachment) |
| [Download Document](actions/download-document.md) | `GET /v4/packages/:packageId/documents/:documentId` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_DownloadDocumentBytes) |
| [Download Package](actions/download-package.md) | `GET /v4/packages/:packageId` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_DownloadPackageBytes) |
| [Fill Form Fields](actions/fill-form-fields.md) | `PUT /v4/packages/:packageId/documents/:documentId/fields` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Fields_FillFormFields) |
| [Get Account](actions/get-account.md) | `GET /v4/account` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Account-Management/operation/V4_Account_GetAccountInformation) |
| [Get Document Details](actions/get-document-details.md) | `GET /v4/packages/:packageId/documents/:documentId/details` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_GetDocumentDetails) |
| [Get Document Verification](actions/get-document-verification.md) | `GET /v4/packages/:packageId/documents/:documentId/verification` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_GetVerification) |
| [Get Package Details](actions/get-package-details.md) | `GET /v4/packages/:packageId/details` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_GetPackageDetails) |
| [Get Package Timeline](actions/get-package-timeline.md) | `GET /v4/packages/:packageId/workflow/timeline` | [docs](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Package/operation/V4_Package_GetPackageTimeline) |
| [Get Package Verification](actions/get-package-verification.md) | `GET /v4/packages/:packageId/verification` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_GetVerification) |
| [Get Signature Settings](actions/get-signature-settings.md) | `GET /v4/settings/signatures` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Personal-Settings/operation/V4_Settings_GetSignatureSettings) |
| [Get Workflow Details](actions/get-workflow-details.md) | `GET /v4/packages/:packageId/workflow` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Workflow_GetWorkflowDetail) |
| [List Attachments](actions/list-attachments.md) | `GET /v4/packages/:packageId/documents/:documentId/attachments` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_GetAttachments) |
| [List Document Fields](actions/list-document-fields.md) | `GET /v4/packages/:packageId/documents/:documentId/fields/:pageNo` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Preparation/operation/V4_Fields_GetAllDocumentFields) |
| [List Packages](actions/list-packages.md) | `GET /v4/packages/:document_status/:pageNo/:recordPerPage` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_GetAllPackages) |
| [List Workflow Users](actions/list-workflow-users.md) | `GET /v4/packages/:packageId/workflow/users` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Workflow_GetWorkflowUsers) |
| [Merge All Documents](actions/merge-all-documents.md) | `POST /v4/packages/:packageId/documents/merge` | [docs](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Package/operation/V4_MergeDocument_MergeAllDocuments) |
| [Move Package To Folder](actions/move-package-to-folder.md) | `PUT /v4/packages/:packageId/move_to` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Folder_MovePackage) |
| [Recall Document](actions/recall-document.md) | `DELETE /v4/packages/:packageId/workflow` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Workflow_RecallWorkflow) |
| [Rename Document](actions/rename-document.md) | `PUT /v4/packages/:packageId/documents/:documentId` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_RenameDocument) |
| [Rename Package](actions/rename-package.md) | `PUT /v4/packages/:packageId` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_RenamePackage) |
| [Send Reminder](actions/send-reminder.md) | `POST /v4/packages/:packageId/workflow/:order/remind` | [docs](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Workflow/operation/Reminder_SendReminder) |
| [Share Document Package](actions/share-document-package.md) | `POST /v4/packages/:packageId/workflow` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Workflow_StartWorkflow) |
| [Sign Document](actions/sign-document.md) | `POST /v4/packages/:packageId/documents/:documentId/sign` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Signing_SignDocument) |
| [Start New Workflow From Existing Package](actions/start-new-workflow-from-existing-package.md) | `POST /v4/packages/:packageId/workflow/new` | [docs](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Package/operation/V4_Package_StartNewWorkflowFromExisting) |
| [Update Document](actions/update-document.md) | `PUT /v4/packages/:packageId/documents/:documentId/update` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UpdateDocument) |
| [Update Workflow User Permissions](actions/update-workflow-user-permissions.md) | `PUT /v4/packages/:packageId/workflow/:order/permissions` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_WorkflowPermission_UpdateWorkflowPermissions) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /v4/packages/:packageId/documents/:documentId/attachments` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_UploadAttachment) |
| [Upload Document](actions/upload-document.md) | `POST /v4/packages/:packageId/documents` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UploadStream) |
| [Upload Document Base64](actions/upload-document-base64.md) | `POST /v4/packages/:packageId/documents/base64` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UploadBase64) |
| [Validate Bulk Sign Packages](actions/validate-bulk-sign-packages.md) | `POST /v4/packages/SIGN/pre` | [docs](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Signing_ValidateBulkSignPackages) |
