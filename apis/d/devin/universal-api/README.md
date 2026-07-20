# Devin: Universal API

AI software engineering agent for creating and managing Devin sessions, knowledge, playbooks, secrets, schedules, and organization resources through the Devin API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/devin/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://devin.ai
- **Vendor API docs:** https://docs.devin.ai/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Self](actions/get-self.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-self?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [List Session Attachments](actions/list-session-attachments.md) | GET | Retrieves session attachments from a Devin session. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Note](actions/create-knowledge-note.md) | POST | Creates a knowledge note in Devin. |
| [Delete Knowledge Note](actions/delete-knowledge-note.md) | DELETE | Deletes an existing knowledge note from Devin. |
| [Get Knowledge Note](actions/get-knowledge-note.md) | GET | Retrieves a knowledge note from Devin. |
| [List Knowledge Notes](actions/list-knowledge-notes.md) | GET | Retrieves a list of knowledge notes from Devin. |
| [Update Knowledge Note](actions/update-knowledge-note.md) | PUT | Updates an existing knowledge note in Devin. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Session Messages](actions/list-session-messages.md) | GET | Retrieves session messages from a Devin session. |
| [Send Session Message](actions/send-session-message.md) | POST | Creates a session message in Devin. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Generate Session Insights](actions/generate-session-insights.md) | POST | Generates session insights for a Devin session. |
| [Get Session Insights](actions/get-session-insights.md) | GET | Retrieves generated session insights from Devin. |

### Runbooks

| Action | Method | Description |
| --- | --- | --- |
| [Create Playbook](actions/create-playbook.md) | POST | Creates a new playbook in Devin. |
| [Delete Playbook](actions/delete-playbook.md) | DELETE | Deletes an existing playbook from Devin. |
| [Get Playbook](actions/get-playbook.md) | GET | Retrieves a playbook record from Devin. |
| [List Playbooks](actions/list-playbooks.md) | GET | Retrieves a list of playbooks from Devin. |
| [Update Playbook](actions/update-playbook.md) | PUT | Updates an existing playbook in Devin. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a new schedule in Devin. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes an existing schedule from Devin. |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves a schedule record from Devin. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves a list of schedules from Devin. |
| [Update Schedule](actions/update-schedule.md) | PUT | Updates an existing schedule in Devin. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Create Secret](actions/create-secret.md) | POST | Creates a new secret in Devin. |
| [Delete Secret](actions/delete-secret.md) | DELETE | Deletes an existing secret from Devin. |
| [List Secrets](actions/list-secrets.md) | GET | Retrieves a list of secrets from Devin. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Archive Session](actions/archive-session.md) | PUT | Archives an existing session in Devin. |
| [Create Session](actions/create-session.md) | POST | Creates a new session in Devin. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session record from Devin. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves a list of sessions from Devin. |
| [List Sessions With Insights](actions/list-sessions-with-insights.md) | GET | Retrieves sessions with insights from Devin. |
| [Terminate Session](actions/terminate-session.md) | DELETE | Deletes an existing session from Devin. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Append Session Tags](actions/append-session-tags.md) | PUT | Updates session tags by appending new tags in Devin. |
| [Get Session Tags](actions/get-session-tags.md) | GET | Retrieves tags for a session in Devin. |
| [Replace Session Tags](actions/replace-session-tags.md) | PUT | Updates session tags by replacing them in Devin. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Self](actions/get-self.md) | GET | Retrieves the authenticated user from Devin. |

