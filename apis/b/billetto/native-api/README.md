# Billetto: Native API Reference

A consolidated summary of Billetto's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://api.billetto.com/reference
- **API base URL:** `https://billetto.dk/api/v3`

## Authentication

### API keypair

Authenticate Billetto requests with the provider-issued Access Key Id and Access Key Secret joined as a single Api-Keypair header value.

### Credentials

- **API Keypair:** `apiKeypair` · required · Billetto API keypair in the exact Access Key Id:Access Key Secret format required by the Api-Keypair header.

Send these headers with each API request:

```http
Api-Keypair: <apiKeypair>
```

[Official authentication documentation](https://api.billetto.com/docs/obtaining-an-api-key)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 0–100).

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Target Group Import](actions/create-target-group-import.md) | `POST organiser/target_group_imports` | [docs](https://api.billetto.com/reference/post-a-target-group-1) |
| [Create Target Group Member](actions/create-target-group-member.md) | `POST organiser/target_group_members` | [docs](https://api.billetto.com/reference/create-a-target-group-member-1) |
| [Create Webhook](actions/create-webhook.md) | `POST organiser/webhooks` | [docs](https://api.billetto.com/reference/create-a-webhook-1) |
| [Delete Target Group](actions/delete-target-group.md) | `DELETE organiser/target_groups/{id}` | [docs](https://api.billetto.com/reference/delete-a-target-group-1) |
| [Delete Target Group Member](actions/delete-target-group-member.md) | `DELETE organiser/target_group_members/{id}` | [docs](https://api.billetto.com/reference/delete-a-target-group-member-1) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE organiser/webhooks/{id}` | [docs](https://api.billetto.com/reference/delete-a-webhook-1) |
| [Email BI Report](actions/email-bi-report.md) | `POST organiser/events/{eventid}/bi_report/by_email/` | [docs](https://api.billetto.com/reference/order-a-business-intelligence-report-sent-to-a-specified-endpoint-1) |
| [Generate Webhook Secret](actions/generate-webhook-secret.md) | `POST organiser/webhooks/{id}/secrets` | [docs](https://api.billetto.com/reference/generate-a-webhook-secret-1) |
| [List Attendees](actions/list-attendees.md) | `GET organiser/attendees` | [docs](https://api.billetto.com/reference/list-attendees-1) |
| [List Campaigns](actions/list-campaigns.md) | `GET organiser/campaigns` | [docs](https://api.billetto.com/reference/list-global-campaigns-1) |
| [List Event Attendees](actions/list-event-attendees.md) | `GET organiser/events/{id}/attendees` | [docs](https://api.billetto.com/reference/list-attendees-on-a-specific-event-1) |
| [List Event Campaigns](actions/list-event-campaigns.md) | `GET organiser/events/{id}/campaigns` | [docs](https://api.billetto.com/reference/list-event-campaigns-1) |
| [List Events](actions/list-events.md) | `GET organiser/events` | [docs](https://api.billetto.com/reference/list-events-1) |
| [List Ledger Entries](actions/list-ledger-entries.md) | `GET organiser/ledger_entries` | [docs](https://api.billetto.com/reference/list-ledger-1) |
| [List Orders](actions/list-orders.md) | `GET organiser/orders` | [docs](https://api.billetto.com/reference/list-orders-1) |
| [List Public Events](actions/list-public-events.md) | `GET public/events` | [docs](https://api.billetto.com/reference/list-public-events-1) |
| [List Import Members](actions/list-target-group-import-members.md) | `GET organiser/target_group_import_members` | [docs](https://api.billetto.com/reference/list-target-group-members-imports-1) |
| [List Target Group Imports](actions/list-target-group-imports.md) | `GET organiser/target_group_imports/{target_group}` | [docs](https://api.billetto.com/reference/list-target-group-import-1) |
| [List Target Group Imports By Target Group](actions/list-target-group-imports-by-target-group.md) | `GET organiser/target_group_imports` | [docs](https://api.billetto.com/reference/list-target-group-import) |
| [List Target Group Members](actions/list-target-group-members.md) | `GET organiser/target_group_members` | [docs](https://api.billetto.com/reference/list-target-group-members-1) |
| [List Target Groups](actions/list-target-groups.md) | `GET organiser/target_groups` | [docs](https://api.billetto.com/reference/list-target-groups-1) |
| [List Ticket Types](actions/list-ticket-types.md) | `GET organiser/ticket_types` | [docs](https://api.billetto.com/reference/list-ticket-types-copy-1) |
| [List Webhooks](actions/list-webhooks.md) | `GET organiser/webhooks` | [docs](https://api.billetto.com/reference/list-webhooks-1) |
| [Retrieve Attendee](actions/retrieve-attendee.md) | `GET organiser/attendees/{id}` | [docs](https://api.billetto.com/reference/retrieve-an-attendee-1) |
| [Retrieve BI Report](actions/retrieve-bi-report.md) | `GET organiser/events/{eventid}/bi_report/` | [docs](https://api.billetto.com/reference/retrieve-business-intelligence-report-in-json-1) |
| [Retrieve Campaign](actions/retrieve-campaign.md) | `GET organiser/campaigns/{id}` | [docs](https://api.billetto.com/reference/retrieve-a-global-campaign-1) |
| [Retrieve Event](actions/retrieve-event.md) | `GET organiser/events/{event_id}` | [docs](https://api.billetto.com/reference/retrieve-an-event-1) |
| [Retrieve Event Campaign](actions/retrieve-event-campaign.md) | `GET organiser/events/{id}/campaigns/{campaign_id}` | [docs](https://api.billetto.com/reference/retrieve-a-campaign-1) |
| [Retrieve Ledger Entry](actions/retrieve-ledger-entry.md) | `GET organiser/ledger_entries/{id}` | [docs](https://api.billetto.com/reference/retrieve-a-ledger-entry-1) |
| [Retrieve Order](actions/retrieve-order.md) | `GET organiser/orders/{id}` | [docs](https://api.billetto.com/reference/retrieve-an-order-1) |
| [Retrieve Public Event](actions/retrieve-public-event.md) | `GET public/events/{id}` | [docs](https://api.billetto.com/reference/retrieve-a-public-events-1) |
| [Retrieve Target Group](actions/retrieve-target-group.md) | `GET organiser/target_groups/{id}` | [docs](https://api.billetto.com/reference/retrieve-a-target-group-1) |
| [Retrieve Webhook](actions/retrieve-webhook.md) | `GET organiser/webhooks/{id}` | [docs](https://api.billetto.com/reference/retrieve-a-webhook-1) |
| [Revoke Webhook Secret](actions/revoke-webhook-secret.md) | `DELETE organiser/webhooks/{webhook_id}/secrets/{id}` | [docs](https://api.billetto.com/reference/revoke-a-webhook-secret-1) |
| [Update Target Group Member](actions/update-target-group-member.md) | `PATCH organiser/target_group_members/{id}` | [docs](https://api.billetto.com/reference/update-a-target-group-member-1) |
| [Update Webhook](actions/update-webhook.md) | `PATCH organiser/webhooks/{id}` | [docs](https://api.billetto.com/reference/update-a-webhook-1) |
