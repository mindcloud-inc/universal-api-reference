# <img src="https://images.mindcloud.co/apps/icons/rossum_1774458270284.png" alt="Rossum logo" width="28" height="28"> Rossum: Universal API

Capture, validate, and automate document workflows with AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rossum/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 66
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rossum.ai/
- **Vendor API docs:** https://rossum.app/api/docs/openapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Current User](actions/retrieve-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (66)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Rossum. |
| [Retrieve Document](actions/retrieve-document.md) | GET | Retrieves a document from Rossum. |
| [Retrieve Document Content](actions/retrieve-document-content.md) | GET | Retrieves original document content from Rossum. |
| [Retrieve Download](actions/retrieve-download.md) | GET | Retrieves a document download from Rossum. |
| [Retrieve Download Content](actions/retrieve-download-content.md) | GET | Retrieves a document download archive from Rossum. |
| [Retrieve Upload](actions/retrieve-upload.md) | GET | Retrieves an upload from Rossum. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Delete Queue](actions/delete-queue.md) | DELETE | Deletes a queue from Rossum. |
| [List Queues](actions/list-queues.md) | GET | Retrieves queues from Rossum. |
| [Retrieve Queue](actions/retrieve-queue.md) | GET | Retrieves a queue from Rossum. |
| [Update Queue](actions/update-queue.md) | PUT | Updates a queue in Rossum. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Rossum. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [List Emails](actions/list-emails.md) | GET | Retrieves emails from Rossum. |
| [Retrieve Email](actions/retrieve-email.md) | GET | Retrieves an email from Rossum. |
| [Retrieve Email Content](actions/retrieve-email-content.md) | GET | Retrieves email content from Rossum. |
| [Retrieve Suggested Email Recipients](actions/retrieve-suggested-email-recipients.md) | GET | Retrieves suggested email recipients for an annotation in Rossum. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List User Roles](actions/list-user-roles.md) | GET | Retrieves user roles from Rossum. |

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox](actions/create-inbox.md) | POST | Creates a new inbox in Rossum. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Rossum. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation](actions/create-annotation.md) | POST | Creates a new annotation in Rossum. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Rossum. |
| [Create Download](actions/create-download.md) | POST | Creates a document download in Rossum. |
| [Import Email](actions/import-email.md) | POST | Imports an email into Rossum. |

### Queue

| Action | Method | Description |
| --- | --- | --- |
| [Create Queue](actions/create-queue.md) | POST | Creates a new queue in Rossum. |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Create Schema](actions/create-schema.md) | POST | Creates a new schema in Rossum. |
| [List Schemas](actions/list-schemas.md) | GET | Retrieves schemas from Rossum. |
| [Retrieve Schema](actions/retrieve-schema.md) | GET | Retrieves a schema from Rossum. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes a label from Rossum. |
| [Update Label](actions/update-label.md) | PUT | Updates a label in Rossum. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a task from Rossum. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Delete Schema](actions/delete-schema.md) | DELETE | Deletes a schema from Rossum. |
| [Update Schema](actions/update-schema.md) | PUT | Updates a schema in Rossum. |
| [Validate Schema](actions/validate-schema.md) | GET | Validates a schema in Rossum. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Assign Annotation](actions/assign-annotation.md) | PUT | Assigns assignees to an annotation in Rossum. |
| [Bulk Update Annotation Content](actions/bulk-update-annotation-content.md) | PUT | Updates annotation content in bulk in Rossum. |
| [Cancel Validation](actions/cancel-validation.md) | PUT | Cancels validation for an annotation in Rossum. |
| [Confirm Annotation](actions/confirm-annotation.md) | PUT | Confirms an annotation in Rossum. |
| [Copy Annotation](actions/copy-annotation.md) | PUT | Copies an annotation to another Rossum queue. |
| [Create Embedded URL](actions/create-embedded-url.md) | POST | Creates an embedded URL for an annotation in Rossum. |
| [Delete Inbox](actions/delete-inbox.md) | DELETE | Deletes an inbox from Rossum. |
| [Export Annotations Cross-Queue](actions/export-annotations-cross-queue.md) | GET | Exports annotations across Rossum queues. |
| [Export Queue Annotations](actions/export-queue-annotations.md) | GET | Exports annotations from a Rossum queue. |
| [List Annotations](actions/list-annotations.md) | GET | Retrieves annotations from Rossum. |
| [List Inboxes](actions/list-inboxes.md) | GET | Retrieves inboxes from Rossum. |
| [Postpone Annotation](actions/postpone-annotation.md) | PUT | Postpones an annotation in Rossum. |
| [Reject Annotation](actions/reject-annotation.md) | PUT | Rejects an annotation in Rossum. |
| [Retrieve Annotation](actions/retrieve-annotation.md) | GET | Retrieves an annotation from Rossum. |
| [Retrieve Annotation Content](actions/retrieve-annotation-content.md) | GET | Retrieves annotation content from Rossum. |
| [Retrieve Inbox](actions/retrieve-inbox.md) | GET | Retrieves an inbox from Rossum. |
| [Retrieve Related Object Counts](actions/retrieve-related-object-counts.md) | GET | Retrieves related object counts for a Rossum queue. |
| [Search Annotations](actions/search-annotations.md) | GET | Finds annotations in Rossum using a complex filter. |
| [Start Validation](actions/start-validation.md) | PUT | Starts validation for an annotation in Rossum. |
| [Update Annotation](actions/update-annotation.md) | PUT | Updates an annotation in Rossum. |
| [Update Annotation Content](actions/update-annotation-content.md) | PUT | Updates annotation content in Rossum. |
| [Update Inbox](actions/update-inbox.md) | PUT | Updates an inbox in Rossum. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload](actions/create-upload.md) | POST | Uploads a document to a Rossum queue. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Rossum. |
| [Retrieve Current User](actions/retrieve-current-user.md) | GET | Retrieves the current user from Rossum. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Rossum. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Rossum. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from Rossum. |
| [Update User](actions/update-user.md) | PUT | Updates a user in Rossum. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Rossum. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Rossum. |
| [Retrieve Workspace](actions/retrieve-workspace.md) | GET | Retrieves a workspace from Rossum. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes a workspace from Rossum. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates a workspace in Rossum. |

