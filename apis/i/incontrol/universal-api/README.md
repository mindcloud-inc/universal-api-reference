# <img src="https://images.mindcloud.co/apps/icons/incontrol-logo-png-seeklogo-71149_1775841033344.png" alt="Incontrol logo" width="28" height="28"> Incontrol: Universal API

Incontrol is a quality and compliance platform for managing organizations, users, forms, drafts, documents, tasks, notifications, and cases.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/incontrol/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://incontrol.app
- **Vendor API docs:** https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Token](actions/verify-api-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/verify-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Case Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Case Note](actions/get-case-note.md) | GET | Retrieves details for a case note from Incontrol. |
| [List Case Notes](actions/list-case-notes.md) | GET | Retrieves a list of case notes from Incontrol. |

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [Get Case](actions/get-case.md) | GET | Retrieves details for a case from Incontrol. |
| [List Cases](actions/list-cases.md) | GET | Retrieves a list of cases from Incontrol. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Download Document](actions/download-document.md) | GET | Downloads a document from Incontrol in the requested file type. |
| [Get Document](actions/get-document.md) | GET | Retrieves details for a document from Incontrol. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from Incontrol. |

### Draft

| Action | Method | Description |
| --- | --- | --- |
| [Get Draft](actions/get-draft.md) | GET | Retrieves details for a draft from Incontrol. |
| [List Drafts](actions/list-drafts.md) | GET | Retrieves a list of drafts from Incontrol. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file from Incontrol. |
| [Get File](actions/get-file.md) | GET | Retrieves details for a file from Incontrol. |

### Form Template

| Action | Method | Description |
| --- | --- | --- |
| [List Form Templates](actions/list-form-templates.md) | GET | Retrieves a list of form templates from Incontrol. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves details for a form from Incontrol. |
| [List Forms](actions/list-forms.md) | GET | Retrieves a list of forms from Incontrol. |

### Local Data Connector

| Action | Method | Description |
| --- | --- | --- |
| [List Local Data Connectors](actions/list-local-data-connectors.md) | GET | Retrieves a list of local data connectors from Incontrol. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification](actions/get-notification.md) | GET | Retrieves details for a notification from Incontrol. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves a list of notifications from Incontrol. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves details for an organization from Incontrol. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Incontrol. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves details for a task from Incontrol. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Incontrol. |

### Test Token

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Token](actions/verify-api-token.md) | GET | Verifies an Incontrol API token and returns its scope. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves details for a user from Incontrol. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Incontrol. |

