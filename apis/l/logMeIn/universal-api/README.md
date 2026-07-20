# <img src="https://images.mindcloud.co/apps/icons/log-me-in_1776113843258.png" alt="LogMeIn logo" width="28" height="28"> LogMeIn: Universal API

LogMeIn Resolve wrapper for sessions, alerts, ticketing, devices, reporting, and knowledge base workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logMeIn/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.logmein.com/products/resolve
- **Vendor API docs:** https://developer.goto.com/LogMeInResolve/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Settings](actions/get-user-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Alerts](actions/acknowledge-alerts.md) | PUT | Updates alerts by acknowledging them in LogMeIn. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves a filtered list of alerts from LogMeIn. |

### Alert Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Alert Subscriptions](actions/list-alert-subscriptions.md) | GET | Retrieves alert webhook subscriptions from LogMeIn. |
| [Upsert Alert Webhook Subscription](actions/upsert-alert-webhook-subscription.md) | PUT | Creates or updates an alert webhook subscription in LogMeIn. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Execute Devices GraphQL Query](actions/execute-devices-graphql-query.md) | GET | Executes a devices GraphQL query in LogMeIn. |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in LogMeIn. |
| [Get Incident](actions/get-incident.md) | GET | Retrieves an existing incident from LogMeIn. |
| [List Incidents](actions/list-incidents.md) | GET | Retrieves a list of incidents from LogMeIn. |
| [Update Incident](actions/update-incident.md) | PUT | Updates an existing incident in LogMeIn. |

### Incident Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Incident Comment](actions/add-incident-comment.md) | POST | Creates a new incident comment in LogMeIn. |
| [Update Incident Comment](actions/update-incident-comment.md) | PUT | Updates an existing incident comment in LogMeIn. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Get User Settings](actions/get-user-settings.md) | GET | Retrieves knowledge base user settings from LogMeIn. |

### Knowledge Base Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new knowledge base document in LogMeIn. |
| [Download Document](actions/download-document.md) | GET | Downloads a knowledge base document from LogMeIn. |
| [Find Related Documents](actions/find-related-documents.md) | GET | Finds related knowledge base documents in LogMeIn. |
| [Find Related Documents By Text](actions/find-related-documents-by-text.md) | GET | Finds related knowledge base documents in LogMeIn by text. |
| [Get Document](actions/get-document.md) | GET | Retrieves a knowledge base document from LogMeIn. |
| [List Documents](actions/list-documents.md) | GET | Retrieves knowledge base documents from LogMeIn. |
| [Move Document](actions/move-document.md) | PUT | Moves an existing knowledge base document in LogMeIn. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing knowledge base document in LogMeIn. |

### Knowledge Base Draft

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Document](actions/create-draft-document.md) | POST | Creates a new draft document in LogMeIn. |
| [Download Draft Document](actions/download-draft-document.md) | GET | Downloads a draft document from LogMeIn. |
| [Get Draft Document](actions/get-draft-document.md) | GET | Retrieves a draft document from LogMeIn. |
| [Get Latest Document Draft](actions/get-latest-document-draft.md) | GET | Retrieves the latest document draft from LogMeIn. |
| [List Draft Documents](actions/list-draft-documents.md) | GET | Retrieves draft knowledge base documents from LogMeIn. |
| [Publish Draft Document](actions/publish-draft-document.md) | PUT | Publishes a draft document in LogMeIn. |
| [Update Draft Document](actions/update-draft-document.md) | PUT | Updates an existing draft document in LogMeIn. |

### Knowledge Base Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new knowledge base folder in LogMeIn. |
| [List Folders](actions/list-folders.md) | GET | Retrieves knowledge base folders from LogMeIn. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing knowledge base folder in LogMeIn. |

### Reporting

| Action | Method | Description |
| --- | --- | --- |
| [Execute Reporting GraphQL Query](actions/execute-reporting-graphql-query.md) | POST | Executes a reporting GraphQL query in LogMeIn. |

### Support Session

| Action | Method | Description |
| --- | --- | --- |
| [Close Session](actions/close-session.md) | PUT | Closes an existing support session in LogMeIn. |
| [Create Support Session](actions/create-support-session.md) | POST | Creates a new support session in LogMeIn. |
| [Get Session Mailto Link](actions/get-session-mailto-link.md) | GET | Retrieves a session email invitation link from LogMeIn. |
| [Get Session State](actions/get-session-state.md) | GET | Retrieves a support session state from LogMeIn. |
| [Send Session SMS Invitation](actions/send-session-sms-invitation.md) | POST | Sends a session SMS invitation from LogMeIn. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [List Tenants](actions/list-tenants.md) | GET | Retrieves a list of tenants from LogMeIn. |

### Ticketing Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticketing Service](actions/get-ticketing-service.md) | GET | Retrieves a ticketing service from LogMeIn. |
| [Get Ticketing Services](actions/get-ticketing-services.md) | GET | Retrieves available ticketing services from LogMeIn. |

### Ticketing User

| Action | Method | Description |
| --- | --- | --- |
| [List Ticketing Users](actions/list-ticketing-users.md) | GET | Retrieves available ticketing users from LogMeIn. |

