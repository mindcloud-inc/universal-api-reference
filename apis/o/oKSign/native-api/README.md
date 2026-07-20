# OKSign: Native API Reference

A consolidated summary of OKSign's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.oksign.be/public/api/
- **API base URL:** `https://www.oksign.be/services/rest/v1`

## Authentication

### API Key

Send the OKSign API key in the custom x-oksign-authorization header. The value combines the account number, authentication token, and organizational token as documented by OKSign.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-oksign-authorization: <apiKey>
```

[Official authentication documentation](https://www.oksign.be/public/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Document Exists](actions/check-document-exists.md) | `GET /document/exists` | [docs](https://www.oksign.be/public/api/#document_exists) |
| [Create Briefcase](actions/create-briefcase.md) | `POST /briefcase/create` | [docs](https://www.oksign.be/public/api/#briefcase_create) |
| [Create Editor Express](actions/create-editor-express.md) | `POST /editorexpress/create` | [docs](https://www.oksign.be/public/api/#editorexpress_create) |
| [Create Sign Express](actions/create-sign-express.md) | `POST /signexpress/create` | [docs](https://www.oksign.be/public/api/#signexpress_create) |
| [List Active Documents](actions/list-active-documents.md) | `GET /documents/active` | [docs](https://www.oksign.be/public/api/#documents_active) |
| [List Signed Documents](actions/list-signed-documents.md) | `GET /documents/signed` | [docs](https://www.oksign.be/public/api/#documents_signed) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/retrieve` | [docs](https://www.oksign.be/public/api/#webhooks_retrieve) |
| [Remove Briefcase](actions/remove-briefcase.md) | `DELETE /briefcase/remove` | [docs](https://www.oksign.be/public/api/#briefcase_remove) |
| [Remove Contacts](actions/remove-contacts.md) | `DELETE /contacts/remove` | [docs](https://www.oksign.be/public/api/#contacts_remove) |
| [Remove Document](actions/remove-document.md) | `DELETE /document/remove` | [docs](https://www.oksign.be/public/api/#document_remove) |
| [Remove Editor Express](actions/remove-editor-express.md) | `DELETE /editorexpress/remove` | [docs](https://www.oksign.be/public/api/#editorexpress_remove) |
| [Remove Email Attachment](actions/remove-email-attachment.md) | `DELETE /emailattachment/remove` | [docs](https://www.oksign.be/public/api/#emailattachment_remove) |
| [Remove Sign Express](actions/remove-sign-express.md) | `DELETE /signexpress/remove` | [docs](https://www.oksign.be/public/api/#signexpress_remove) |
| [Retrieve Audit Trail](actions/retrieve-audit-trail.md) | `GET /audittrail/retrieve` | [docs](https://www.oksign.be/public/api/#audittrail_retrieve) |
| [Retrieve Briefcase](actions/retrieve-briefcase.md) | `GET /briefcase/retrieve` | [docs](https://www.oksign.be/public/api/#briefcase_retrieve) |
| [Retrieve Contacts](actions/retrieve-contacts.md) | `GET /contacts/retrieve` | [docs](https://www.oksign.be/public/api/#contacts_retrieve) |
| [Retrieve Credits](actions/retrieve-credits.md) | `GET /credits/retrieve` | [docs](https://www.oksign.be/public/api/#credits_retrieve) |
| [Retrieve Document](actions/retrieve-document.md) | `GET /document/retrieve` | [docs](https://www.oksign.be/public/api/#document_retrieve) |
| [Retrieve Editor Express](actions/retrieve-editor-express.md) | `GET /editorexpress/retrieve` | [docs](https://www.oksign.be/public/api/#editorexpress_retrieve) |
| [Retrieve Email Templates](actions/retrieve-email-templates.md) | `GET /emailtemplates/retrieve` | [docs](https://www.oksign.be/public/api/#emailtemplates_retrieve) |
| [Retrieve Form Descriptor](actions/retrieve-form-descriptor.md) | `GET /formdesc/retrieve` | [docs](https://www.oksign.be/public/api/#formdesc_retrieve) |
| [Retrieve Linked List](actions/retrieve-linked-list.md) | `GET /linkedlist/retrieve` | [docs](https://www.oksign.be/public/api/#linkedlist_retrieve) |
| [Retrieve Metadata](actions/retrieve-metadata.md) | `GET /metadata/retrieve/v2` | [docs](https://www.oksign.be/public/api/#metadata_retrieve_v2) |
| [Retrieve Sign Express](actions/retrieve-sign-express.md) | `GET /signexpress/retrieve` | [docs](https://www.oksign.be/public/api/#signexpress_retrieve) |
| [Retrieve Users](actions/retrieve-users.md) | `GET /users/retrieve` | [docs](https://www.oksign.be/public/api/#users_retrieve) |
| [Update Organization Token Info](actions/update-organization-token-info.md) | `POST /orgtokeninfo/update` | [docs](https://www.oksign.be/public/api/#orgtokeninfo_update) |
| [Upload Contacts](actions/upload-contacts.md) | `POST /contacts/upload` | [docs](https://www.oksign.be/public/api/#contacts_upload) |
| [Upload Document](actions/upload-document.md) | `POST /document/upload` | [docs](https://www.oksign.be/public/api/#document_upload) |
| [Upload Email Attachment](actions/upload-email-attachment.md) | `POST /emailattachment/upload` | [docs](https://www.oksign.be/public/api/#emailattachment_upload) |
| [Upload Form Descriptor](actions/upload-form-descriptor.md) | `POST /formdesc/upload` | [docs](https://www.oksign.be/public/api/#formdesc_upload) |
| [Upload Notifications](actions/upload-notifications.md) | `POST /notifications/upload` | [docs](https://www.oksign.be/public/api/#notifications_upload) |
