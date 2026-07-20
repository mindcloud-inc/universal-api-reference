# Leadspicker: Native API Reference

A consolidated summary of Leadspicker's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.leadspicker.com/app/sb/api/docs
- **OpenAPI specification:** https://app.leadspicker.com/app/sb/api/openapi.json
- **API base URL:** `https://app.leadspicker.com`

## Authentication

### API Key

Authenticate Leadspicker API requests with a Leadspicker API key. The OpenAPI definition supports API key authentication with the X-API-Key header and bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://app.leadspicker.com/app/sb/api/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–200).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User Info](actions/get-current-user-info.md) | `GET /app/sb/api/auth/me` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Auth/apps_salesbooster_api_me) |
| [Get Dashboard Statistics](actions/get-dashboard-statistics.md) | `GET /app/sb/api/dashboard/stats` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Dashboard/apps_salesbooster_api_get_dashboard_stats) |
| [Get Person](actions/get-person.md) | `GET /app/sb/api/persons/:person_id` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Person/apps_salesbooster_api_person_detail) |
| [Get Person Communication](actions/get-person-communication.md) | `GET /app/sb/api/persons/:person_id/communication` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Communication/apps_salesbooster_api_person_communication) |
| [Get Person Summary](actions/get-person-summary.md) | `GET /app/sb/api/persons-simple/:person_id` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Person/apps_salesbooster_api_persons_simple_detail) |
| [Get Project](actions/get-project.md) | `GET /app/sb/api/projects/:project_id` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Project/apps_salesbooster_api_project_detail) |
| [Get Project Statistics](actions/get-project-statistics.md) | `GET /app/sb/api/projects/:project_id/sequence-stats` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Project/apps_salesbooster_api_project_sequence_stats_detail) |
| [Get Sequence Message](actions/get-sequence-message.md) | `GET /app/sb/api/sequence/:sequence_id` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Email%20Sequence/apps_salesbooster_api_sequence_detail) |
| [List API Changelog Entries](actions/list-api-changelog-entries.md) | `GET /app/sb/api/api-changelog` | [docs](https://app.leadspicker.com/app/sb/api/docs#/API%20Changelog/apps_salesbooster_api_list_api_changelog) |
| [List Dashboard Event Types](actions/list-dashboard-event-types.md) | `GET /app/sb/api/dashboard/event-types` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Dashboard/apps_salesbooster_api_dashboard_event_types) |
| [List Dashboard Timeline Events](actions/list-dashboard-timeline-events.md) | `GET /app/sb/api/dashboard/logs` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Dashboard/apps_salesbooster_api_dashboard_logs) |
| [List Email Accounts](actions/list-email-accounts.md) | `GET /app/sb/api/email-accounts` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Outreach%20Accounts/apps_salesbooster_api_email_accounts) |
| [List Inbound Message Signatures](actions/list-inbound-message-signatures.md) | `GET /app/sb/api/inbound-messages/signatures` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Replies/apps_salesbooster_api_inbound_message_signatures) |
| [List Inbound Messages](actions/list-inbound-messages.md) | `GET /app/sb/api/inbound-messages` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Replies/apps_salesbooster_api_inbound_messages) |
| [List LinkedIn Accounts](actions/list-linkedin-accounts.md) | `GET /app/sb/api/linkedin-accounts` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Outreach%20Accounts/apps_salesbooster_api_linkedin_accounts) |
| [List Notifications](actions/list-notifications.md) | `GET /app/sb/api/notifications` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Notifications/apps_salesbooster_api_notifications_list) |
| [List Person Labels](actions/list-person-labels.md) | `GET /app/sb/api/person-labels` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Person%20Labels/apps_salesbooster_api_person_labels) |
| [List Persons](actions/list-persons.md) | `GET /app/sb/api/persons-simple` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Person/apps_salesbooster_api_persons_simple) |
| [List Project People](actions/list-project-people.md) | `GET /app/sb/api/projects/:project_id/people` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Project%20Persons/apps_salesbooster_api_projects_people_list) |
| [List Project Timeline Events](actions/list-project-timeline-events.md) | `GET /app/sb/api/projects/:project_id/events` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Project/apps_salesbooster_api_project_events) |
| [List Projects](actions/list-projects.md) | `GET /app/sb/api/projects` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Project/apps_salesbooster_api_get_project_list) |
| [List Sequence Messages](actions/list-sequence-messages.md) | `GET /app/sb/api/sequence` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Email%20Sequence/apps_salesbooster_api_sequence_list) |
| [List Sequence Templates](actions/list-sequence-templates.md) | `GET /app/sb/api/sequence/templates` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Email%20Sequence/apps_salesbooster_api_sequence_template_list) |
| [List Webhooks](actions/list-webhooks.md) | `GET /app/sb/api/webhooks` | [docs](https://app.leadspicker.com/app/sb/api/docs#/Notifications/apps_salesbooster_api_webhook_list) |
