# Billetweb: Native API Reference

A consolidated summary of Billetweb's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.billetweb.fr/bo/api.php
- **API base URL:** `https://www.billetweb.fr/api`

## Authentication

### Billetweb API Token

Paste the Billetweb API token exactly as shown on the API page. MindCloud sends it as Authorization: Basic <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.billetweb.fr/bo/api.php)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add List Entry](actions/add-list-entry.md) | `POST /list/:id/push` | [docs](https://www.billetweb.fr/bo/api.php#/api/list/:id/push) |
| [Add Offline Order](actions/add-offline-order.md) | `POST /event/:id/add_order` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/add_order) |
| [Create Event From Template](actions/create-event-from-template.md) | `POST /event/:id/clone` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/clone) |
| [Create Or Update Event Sessions](actions/create-or-update-event-sessions.md) | `POST /event/:id/dates_update` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/dates_update) |
| [Create Or Update Event Tickets](actions/create-or-update-event-tickets.md) | `POST /event/:id/tickets_update` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/tickets_update) |
| [Get Campaign Content](actions/get-campaign-content.md) | `GET /campaign/:id/data` | [docs](https://www.billetweb.fr/bo/api.php#/api/campaigns/:id/data) |
| [Get List Content](actions/get-list-content.md) | `GET /list/:id/data` | [docs](https://www.billetweb.fr/bo/api.php#/api/lists/:id/data) |
| [List Accounting Entries](actions/list-accounting-entries.md) | `GET /accounting` | [docs](https://www.billetweb.fr/bo/api.php#/api/accounting) |
| [List All Attendees](actions/list-all-attendees.md) | `GET /attendees` | [docs](https://www.billetweb.fr/bo/api.php#/api/attendees) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://www.billetweb.fr/bo/api.php#/api/campaigns) |
| [List CRM Contacts](actions/list-crm-contacts.md) | `GET /crm/contacts` | [docs](https://www.billetweb.fr/bo/api.php#/api/crm/contacts) |
| [List CRM Segments](actions/list-crm-segments.md) | `GET /crm/segments` | [docs](https://www.billetweb.fr/bo/api.php#/api/crm/segments) |
| [List Event Attendees](actions/list-event-attendees.md) | `GET /event/:id/attendees` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/attendees) |
| [List Event Availability](actions/list-event-availability.md) | `GET /event/:id/avail` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/avail) |
| [List Event Sessions](actions/list-event-sessions.md) | `GET /event/:id/dates` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/dates) |
| [List Event Tickets](actions/list-event-tickets.md) | `GET /event/:id/tickets` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/tickets) |
| [List Event Waiting List](actions/list-event-waiting-list.md) | `GET /event/:id/waiting` | [docs](https://www.billetweb.fr/bo/api.php#/api/event/:id/waiting) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://www.billetweb.fr/bo/api.php) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://www.billetweb.fr/bo/api.php#/api/lists) |
| [List Payouts](actions/list-payouts.md) | `GET /payouts` | [docs](https://www.billetweb.fr/bo/api.php#/api/payouts) |
| [List Session Changes](actions/list-session-changes.md) | `GET /date_changes` | [docs](https://www.billetweb.fr/bo/api.php#/api/date_changes) |
| [List Shared Forms](actions/list-shared-forms.md) | `GET /forms` | [docs](https://www.billetweb.fr/bo/api.php#/api/forms) |
| [Replace List Contents](actions/replace-list-contents.md) | `POST /list/:id/replace` | [docs](https://www.billetweb.fr/bo/api.php#/api/list/:id/replace) |
