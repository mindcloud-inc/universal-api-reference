# <img src="https://images.mindcloud.co/apps/icons/billetto_1776861150180.png" alt="Billetto logo" width="28" height="28"> Billetto: Universal API

Billetto is an event ticketing platform for organizers, audiences, public event discovery, reporting, webhooks, and target group management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billetto/latest
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://billetto.dk
- **Vendor API docs:** https://api.billetto.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Public Events](actions/list-public-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-public-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [List Attendees](actions/list-attendees.md) | GET | Retrieves attendees from Billetto. |
| [List Event Attendees](actions/list-event-attendees.md) | GET | Retrieves attendees for an event from Billetto. |
| [Retrieve Attendee](actions/retrieve-attendee.md) | GET | Retrieves an attendee from Billetto. |

### Business Intelligence Report

| Action | Method | Description |
| --- | --- | --- |
| [Email BI Report](actions/email-bi-report.md) | POST | Sends a business intelligence report from Billetto by email. |
| [Retrieve BI Report](actions/retrieve-bi-report.md) | GET | Retrieves a business intelligence report from Billetto in JSON. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Billetto. |
| [List Event Campaigns](actions/list-event-campaigns.md) | GET | Retrieves campaigns for an event from Billetto. |
| [Retrieve Campaign](actions/retrieve-campaign.md) | GET | Retrieves a campaign from Billetto. |
| [Retrieve Event Campaign](actions/retrieve-event-campaign.md) | GET | Retrieves an event campaign from Billetto. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from Billetto. |
| [Retrieve Event](actions/retrieve-event.md) | GET | Retrieves an event from Billetto. |

### Ledger Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Entries](actions/list-ledger-entries.md) | GET | Retrieves ledger entries from Billetto. |
| [Retrieve Ledger Entry](actions/retrieve-ledger-entry.md) | GET | Retrieves a ledger entry from Billetto. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Billetto. |
| [Retrieve Order](actions/retrieve-order.md) | GET | Retrieves an order from Billetto. |

### Public Event

| Action | Method | Description |
| --- | --- | --- |
| [List Public Events](actions/list-public-events.md) | GET | Retrieves public events from Billetto. |
| [Retrieve Public Event](actions/retrieve-public-event.md) | GET | Retrieves a public event from Billetto. |

### Target Group

| Action | Method | Description |
| --- | --- | --- |
| [Delete Target Group](actions/delete-target-group.md) | DELETE | Deletes a target group from Billetto. |
| [List Target Groups](actions/list-target-groups.md) | GET | Retrieves target groups from Billetto. |
| [Retrieve Target Group](actions/retrieve-target-group.md) | GET | Retrieves a target group from Billetto. |

### Target Group Import

| Action | Method | Description |
| --- | --- | --- |
| [Create Target Group Import](actions/create-target-group-import.md) | POST | Creates a target group import in Billetto. |
| [List Target Group Imports](actions/list-target-group-imports.md) | GET | Retrieves imports for a target group from Billetto. |
| [List Target Group Imports By Target Group](actions/list-target-group-imports-by-target-group.md) | GET | Retrieves target group imports from Billetto by target group. |

### Target Group Import Member

| Action | Method | Description |
| --- | --- | --- |
| [List Import Members](actions/list-target-group-import-members.md) | GET | Retrieves target group import members from Billetto. |

### Target Group Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Target Group Member](actions/create-target-group-member.md) | POST | Creates a target group member in Billetto. |
| [Delete Target Group Member](actions/delete-target-group-member.md) | DELETE | Deletes a target group member from Billetto. |
| [List Target Group Members](actions/list-target-group-members.md) | GET | Retrieves target group members from Billetto. |
| [Update Target Group Member](actions/update-target-group-member.md) | PUT | Updates a target group member in Billetto. |

### Ticket Type

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Types](actions/list-ticket-types.md) | GET | Retrieves ticket types from Billetto. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Billetto. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Billetto. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Billetto. |
| [Retrieve Webhook](actions/retrieve-webhook.md) | GET | Retrieves a webhook from Billetto. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in Billetto. |

### Webhook Secret

| Action | Method | Description |
| --- | --- | --- |
| [Generate Webhook Secret](actions/generate-webhook-secret.md) | POST | Creates a webhook secret in Billetto. |
| [Revoke Webhook Secret](actions/revoke-webhook-secret.md) | DELETE | Deletes a webhook secret from Billetto. |

