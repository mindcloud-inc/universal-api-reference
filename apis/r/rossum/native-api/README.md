# Rossum: Native API Reference

A consolidated summary of Rossum's API configuration and 66 documented operations, with links to official documentation.

- **Official docs:** https://rossum.app/api/docs/openapi/
- **OpenAPI specification:** https://rossum.app/api/docs/openapi/openapi-specs/openapi.json
- **API base URL:** `https://mindcloud.rossum.app/api/v1`

## Authentication

### Bearer Token

Use a Rossum API bearer token obtained from the login flow.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://knowledge-base.rossum.ai/docs/getting-started-with-rossum)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 20; maximum 100). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (66 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Annotation](actions/assign-annotation.md) | `POST /annotations/assign` | [docs](https://rossum.app/api/docs/openapi/) |
| [Bulk Update Annotation Content](actions/bulk-update-annotation-content.md) | `POST /annotations/:annotationID/content/operations` | [docs](https://rossum.app/api/docs/openapi/) |
| [Cancel Validation](actions/cancel-validation.md) | `POST /annotations/:annotationID/cancel` | [docs](https://rossum.app/api/docs/openapi/) |
| [Confirm Annotation](actions/confirm-annotation.md) | `POST /annotations/:annotationID/confirm` | [docs](https://rossum.app/api/docs/openapi/) |
| [Copy Annotation](actions/copy-annotation.md) | `POST /annotations/:annotationID/copy` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Annotation](actions/create-annotation.md) | `POST /annotations` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Download](actions/create-download.md) | `POST /documents/downloads` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Embedded URL](actions/create-embedded-url.md) | `POST /annotations/:annotationID/create_embedded_url` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Inbox](actions/create-inbox.md) | `POST /inboxes` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Label](actions/create-label.md) | `POST /labels` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Queue](actions/create-queue.md) | `POST /queues` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Schema](actions/create-schema.md) | `POST /schemas` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Upload](actions/create-upload.md) | `POST /uploads` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://rossum.app/api/docs/openapi/) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://rossum.app/api/docs/openapi/) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:documentID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Delete Inbox](actions/delete-inbox.md) | `DELETE /inboxes/:inboxID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Delete Label](actions/delete-label.md) | `DELETE /labels/:labelID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Delete Queue](actions/delete-queue.md) | `DELETE /queues/:id` | [docs](https://rossum.app/api/docs/openapi/) |
| [Delete Schema](actions/delete-schema.md) | `DELETE /schemas/:schemaID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:userID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /workspaces/:workspaceID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Export Annotations Cross-Queue](actions/export-annotations-cross-queue.md) | `POST /annotations/export` | [docs](https://rossum.app/api/docs/openapi/) |
| [Export Queue Annotations](actions/export-queue-annotations.md) | `GET /queues/:id/export` | [docs](https://rossum.app/api/docs/openapi/) |
| [Import Email](actions/import-email.md) | `POST /emails/import` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Annotations](actions/list-annotations.md) | `GET /annotations` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Emails](actions/list-emails.md) | `GET /emails` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Inboxes](actions/list-inboxes.md) | `GET /inboxes` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Queues](actions/list-queues.md) | `GET /queues` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Schemas](actions/list-schemas.md) | `GET /schemas` | [docs](https://rossum.app/api/docs/openapi/) |
| [List User Roles](actions/list-user-roles.md) | `GET /groups` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://rossum.app/api/docs/openapi/) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://rossum.app/api/docs/openapi/) |
| [Postpone Annotation](actions/postpone-annotation.md) | `POST /annotations/:annotationID/postpone` | [docs](https://rossum.app/api/docs/openapi/) |
| [Reject Annotation](actions/reject-annotation.md) | `POST /annotations/:annotationID/reject` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Annotation](actions/retrieve-annotation.md) | `GET /annotations/:annotationID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Annotation Content](actions/retrieve-annotation-content.md) | `GET /annotations/:annotationID/content` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Current User](actions/retrieve-current-user.md) | `GET /auth/user` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Document](actions/retrieve-document.md) | `GET /documents/:documentID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Document Content](actions/retrieve-document-content.md) | `GET /documents/:documentID/content` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Download](actions/retrieve-download.md) | `GET /documents/downloads/:documentsDownloadID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Download Content](actions/retrieve-download-content.md) | `GET /documents/downloads/:documentsDownloadID/content` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Email](actions/retrieve-email.md) | `GET /emails/:emailID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Email Content](actions/retrieve-email-content.md) | `GET /emails/:emailID/content` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Inbox](actions/retrieve-inbox.md) | `GET /inboxes/:inboxID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Queue](actions/retrieve-queue.md) | `GET /queues/:id` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Related Object Counts](actions/retrieve-related-object-counts.md) | `GET /queues/:id/related_objects_counts` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Schema](actions/retrieve-schema.md) | `GET /schemas/:schemaID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Suggested Email Recipients](actions/retrieve-suggested-email-recipients.md) | `POST /annotations/suggested_recipients` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /tasks/:taskID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Upload](actions/retrieve-upload.md) | `GET /uploads/:uploadID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:userID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Retrieve Workspace](actions/retrieve-workspace.md) | `GET /workspaces/:workspaceID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Search Annotations](actions/search-annotations.md) | `POST /annotations/search` | [docs](https://rossum.app/api/docs/openapi/) |
| [Start Validation](actions/start-validation.md) | `POST /annotations/:annotationID/start` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update Annotation](actions/update-annotation.md) | `PATCH /annotations/:annotationID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update Annotation Content](actions/update-annotation-content.md) | `PATCH /annotations/:annotationID/content` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update Inbox](actions/update-inbox.md) | `PATCH /inboxes/:inboxID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update Label](actions/update-label.md) | `PATCH /labels/:labelID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update Queue](actions/update-queue.md) | `PATCH /queues/:id` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update Schema](actions/update-schema.md) | `PATCH /schemas/:schemaID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update User](actions/update-user.md) | `PATCH /users/:userID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /workspaces/:workspaceID` | [docs](https://rossum.app/api/docs/openapi/) |
| [Validate Schema](actions/validate-schema.md) | `POST /schemas/validate` | [docs](https://rossum.app/api/docs/openapi/) |
