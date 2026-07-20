# Devin: Native API Reference

A consolidated summary of Devin's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.devin.ai/api-reference/overview
- **API base URL:** `https://api.devin.ai`

## Authentication

### Service User API Key

Authenticate to Devin with a service user API key. Devin v3 API requests use an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.devin.ai/api-reference/authentication)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `end_cursor`.

## Pagination

Use `first` in the query string to set the page size (default 50; accepted range 1–200). Use `after` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Append Session Tags](actions/append-session-tags.md) | `POST /v3/organizations/:org_id/sessions/:devin_id/tags` | [docs](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-tags) |
| [Archive Session](actions/archive-session.md) | `POST /v3/organizations/:org_id/sessions/:devin_id/archive` | [docs](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-archive) |
| [Create Knowledge Note](actions/create-knowledge-note.md) | `POST /v3/organizations/:org_id/knowledge/notes` | [docs](https://docs.devin.ai/api-reference/v3/notes/post-organizations-knowledge-notes) |
| [Create Playbook](actions/create-playbook.md) | `POST /v3/organizations/:org_id/playbooks` | [docs](https://docs.devin.ai/api-reference/v3/playbooks/post-organizations-playbooks) |
| [Create Schedule](actions/create-schedule.md) | `POST /v3/organizations/:org_id/schedules` | [docs](https://docs.devin.ai/api-reference/v3/schedules/post-organizations-schedules) |
| [Create Secret](actions/create-secret.md) | `POST /v3/organizations/:org_id/secrets` | [docs](https://docs.devin.ai/api-reference/v3/secrets/post-organizations-secrets) |
| [Create Session](actions/create-session.md) | `POST /v3/organizations/:org_id/sessions` | [docs](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-sessions) |
| [Delete Knowledge Note](actions/delete-knowledge-note.md) | `DELETE /v3/organizations/:org_id/knowledge/notes/:note_id` | [docs](https://docs.devin.ai/api-reference/v3/notes/delete-organizations-knowledge-notes-note-id) |
| [Delete Playbook](actions/delete-playbook.md) | `DELETE /v3/organizations/:org_id/playbooks/:playbook_id` | [docs](https://docs.devin.ai/api-reference/v3/playbooks/delete-organizations-playbooks-playbook-id) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /v3/organizations/:org_id/schedules/:schedule_id` | [docs](https://docs.devin.ai/api-reference/v3/schedules/delete-organizations-schedule) |
| [Delete Secret](actions/delete-secret.md) | `DELETE /v3/organizations/:org_id/secrets/:secret_id` | [docs](https://docs.devin.ai/api-reference/v3/secrets/delete-organizations-secrets) |
| [Generate Session Insights](actions/generate-session-insights.md) | `POST /v3/organizations/:org_id/sessions/:devin_id/insights/generate` | [docs](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-insights-generate) |
| [Get Knowledge Note](actions/get-knowledge-note.md) | `GET /v3/organizations/:org_id/knowledge/notes/:note_id` | [docs](https://docs.devin.ai/api-reference/v3/notes/get-organizations-knowledge-notes-note-id) |
| [Get Playbook](actions/get-playbook.md) | `GET /v3/organizations/:org_id/playbooks/:playbook_id` | [docs](https://docs.devin.ai/api-reference/v3/playbooks/get-organizations-playbooks-playbook-id) |
| [Get Schedule](actions/get-schedule.md) | `GET /v3/organizations/:org_id/schedules/:schedule_id` | [docs](https://docs.devin.ai/api-reference/v3/schedules/get-organizations-schedule) |
| [Get Self](actions/get-self.md) | `GET /v3/self` | [docs](https://docs.devin.ai/api-reference/v3/self/self) |
| [Get Session](actions/get-session.md) | `GET /v3/organizations/:org_id/sessions/:devin_id` | [docs](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session) |
| [Get Session Insights](actions/get-session-insights.md) | `GET /v3/organizations/:org_id/sessions/:devin_id/insights` | [docs](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session-insights) |
| [Get Session Tags](actions/get-session-tags.md) | `GET /v3/organizations/:org_id/sessions/:devin_id/tags` | [docs](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session-tags) |
| [List Knowledge Notes](actions/list-knowledge-notes.md) | `GET /v3/organizations/:org_id/knowledge/notes` | [docs](https://docs.devin.ai/api-reference/v3/notes/organizations-knowledge-notes) |
| [List Playbooks](actions/list-playbooks.md) | `GET /v3/organizations/:org_id/playbooks` | [docs](https://docs.devin.ai/api-reference/v3/playbooks/organizations-playbooks) |
| [List Schedules](actions/list-schedules.md) | `GET /v3/organizations/:org_id/schedules` | [docs](https://docs.devin.ai/api-reference/v3/schedules/organizations-schedules) |
| [List Secrets](actions/list-secrets.md) | `GET /v3/organizations/:org_id/secrets` | [docs](https://docs.devin.ai/api-reference/v3/secrets/organizations-secrets) |
| [List Session Attachments](actions/list-session-attachments.md) | `GET /v3/organizations/:org_id/sessions/:devin_id/attachments` | [docs](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session-attachments) |
| [List Session Messages](actions/list-session-messages.md) | `GET /v3/organizations/:org_id/sessions/:devin_id/messages` | [docs](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session-messages) |
| [List Sessions](actions/list-sessions.md) | `GET /v3/organizations/:org_id/sessions` | [docs](https://docs.devin.ai/api-reference/v3/sessions/enterprise-sessions) |
| [List Sessions With Insights](actions/list-sessions-with-insights.md) | `GET /v3/organizations/:org_id/sessions/insights` | [docs](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-sessions-insights) |
| [Replace Session Tags](actions/replace-session-tags.md) | `PUT /v3/organizations/:org_id/sessions/:devin_id/tags` | [docs](https://docs.devin.ai/api-reference/v3/sessions/put-organizations-session-tags) |
| [Send Session Message](actions/send-session-message.md) | `POST /v3/organizations/:org_id/sessions/:devin_id/messages` | [docs](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-message) |
| [Terminate Session](actions/terminate-session.md) | `DELETE /v3/organizations/:org_id/sessions/:devin_id` | [docs](https://docs.devin.ai/api-reference/v3/sessions/delete-organizations-sessions) |
| [Update Knowledge Note](actions/update-knowledge-note.md) | `PUT /v3/organizations/:org_id/knowledge/notes/:note_id` | [docs](https://docs.devin.ai/api-reference/v3/notes/put-organizations-knowledge-notes-note-id) |
| [Update Playbook](actions/update-playbook.md) | `PUT /v3/organizations/:org_id/playbooks/:playbook_id` | [docs](https://docs.devin.ai/api-reference/v3/playbooks/put-organizations-playbooks-playbook-id) |
| [Update Schedule](actions/update-schedule.md) | `PATCH /v3/organizations/:org_id/schedules/:schedule_id` | [docs](https://docs.devin.ai/api-reference/v3/schedules/patch-organizations-schedule) |
