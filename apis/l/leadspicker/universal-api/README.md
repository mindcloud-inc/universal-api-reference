# <img src="https://images.mindcloud.co/apps/icons/leadspicker-icon_1778172207416.png" alt="Leadspicker logo" width="28" height="28"> Leadspicker: Universal API

Leadspicker is a sales automation and lead generation platform for finding prospects, managing outreach projects, tracking engagement, and working with sequences, replies, accounts, and enrichment data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadspicker/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leadspicker.com
- **Vendor API docs:** https://app.leadspicker.com/app/sb/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Info](actions/get-current-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Api Changelog Entry

| Action | Method | Description |
| --- | --- | --- |
| [List API Changelog Entries](actions/list-api-changelog-entries.md) | GET | Retrieves API changelog entries from Leadspicker. |

### Dashboard Event Type

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboard Event Types](actions/list-dashboard-event-types.md) | GET | Retrieves dashboard timeline event types from Leadspicker. |

### Dashboard Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard Statistics](actions/get-dashboard-statistics.md) | GET | Retrieves dashboard statistics from Leadspicker. |

### Dashboard Timeline Event

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboard Timeline Events](actions/list-dashboard-timeline-events.md) | GET | Retrieves dashboard timeline events from Leadspicker. |

### Email Account

| Action | Method | Description |
| --- | --- | --- |
| [List Email Accounts](actions/list-email-accounts.md) | GET | Retrieves email accounts from Leadspicker. |

### Inbound Message

| Action | Method | Description |
| --- | --- | --- |
| [List Inbound Messages](actions/list-inbound-messages.md) | GET | Retrieves inbound messages from Leadspicker. |

### Inbound Message Signature

| Action | Method | Description |
| --- | --- | --- |
| [List Inbound Message Signatures](actions/list-inbound-message-signatures.md) | GET | Retrieves inbound message signatures from Leadspicker. |

### Linkedin Account

| Action | Method | Description |
| --- | --- | --- |
| [List LinkedIn Accounts](actions/list-linkedin-accounts.md) | GET | Retrieves LinkedIn accounts from Leadspicker. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Leadspicker. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Leadspicker. |
| [Get Person Summary](actions/get-person-summary.md) | GET | Retrieves a simplified person record from Leadspicker. |
| [List Persons](actions/list-persons.md) | GET | Retrieves persons from Leadspicker. |

### Person Communication

| Action | Method | Description |
| --- | --- | --- |
| [Get Person Communication](actions/get-person-communication.md) | GET | Retrieves communication for a person in Leadspicker. |

### Person Label

| Action | Method | Description |
| --- | --- | --- |
| [List Person Labels](actions/list-person-labels.md) | GET | Retrieves person labels from Leadspicker. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Leadspicker. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Leadspicker. |

### Project Person

| Action | Method | Description |
| --- | --- | --- |
| [List Project People](actions/list-project-people.md) | GET | Retrieves people for a project in Leadspicker. |

### Project Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Statistics](actions/get-project-statistics.md) | GET | Retrieves sequence statistics for a project in Leadspicker. |

### Project Timeline Event

| Action | Method | Description |
| --- | --- | --- |
| [List Project Timeline Events](actions/list-project-timeline-events.md) | GET | Retrieves timeline events for a project in Leadspicker. |

### Sequence Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequence Message](actions/get-sequence-message.md) | GET | Retrieves a sequence message from Leadspicker. |
| [List Sequence Messages](actions/list-sequence-messages.md) | GET | Retrieves sequence messages from Leadspicker. |

### Sequence Template

| Action | Method | Description |
| --- | --- | --- |
| [List Sequence Templates](actions/list-sequence-templates.md) | GET | Retrieves sequence templates from Leadspicker. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Info](actions/get-current-user-info.md) | GET | Retrieves current user information from Leadspicker. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Leadspicker. |

