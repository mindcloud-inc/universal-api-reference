# <img src="https://images.mindcloud.co/apps/icons/billetweb_1773851131572.png" alt="Billetweb logo" width="28" height="28"> Billetweb: Universal API

Manage events, ticket sales, attendees, and payouts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billetweb/latest
- **Category:** Support / Ticketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.billetweb.fr
- **Vendor API docs:** https://www.billetweb.fr/bo/api.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Accounting Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Accounting Entries](actions/list-accounting-entries.md) | GET | Retrieves accounting entries from your Billetweb account. |

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [List All Attendees](actions/list-all-attendees.md) | GET | Retrieves attendees across all Billetweb events. |
| [List Event Attendees](actions/list-event-attendees.md) | GET | Retrieves attendees for a Billetweb event. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Content](actions/get-campaign-content.md) | GET | Retrieves campaign content from your Billetweb account. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from your Billetweb account. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List CRM Contacts](actions/list-crm-contacts.md) | GET | Retrieves CRM contacts from your Billetweb account. |

### Date Change

| Action | Method | Description |
| --- | --- | --- |
| [List Session Changes](actions/list-session-changes.md) | GET | Retrieves session changes from your Billetweb account. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from your Billetweb account. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event From Template](actions/create-event-from-template.md) | POST | Creates a new event in Billetweb from a template. |
| [List Event Availability](actions/list-event-availability.md) | GET | Retrieves availability for a Billetweb event. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Forms](actions/list-shared-forms.md) | GET | Retrieves shared forms from your Billetweb account. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Add List Entry](actions/add-list-entry.md) | POST | Adds an entry to a Billetweb list. |
| [Get List Content](actions/get-list-content.md) | GET | Retrieves the contents of a Billetweb list. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from your Billetweb account. |
| [Replace List Contents](actions/replace-list-contents.md) | PUT | Replaces the contents of a Billetweb list. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Add Offline Order](actions/add-offline-order.md) | POST | Creates a new offline order in Billetweb. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts from your Billetweb account. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List CRM Segments](actions/list-crm-segments.md) | GET | Retrieves CRM segments from your Billetweb account. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Event Sessions](actions/create-or-update-event-sessions.md) | PUT | Creates or updates event sessions in Billetweb. |
| [List Event Sessions](actions/list-event-sessions.md) | GET | Retrieves sessions for a Billetweb event. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [List Event Waiting List](actions/list-event-waiting-list.md) | GET | Retrieves the waiting list for a Billetweb event. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Event Tickets](actions/create-or-update-event-tickets.md) | PUT | Creates or updates event tickets in Billetweb. |
| [List Event Tickets](actions/list-event-tickets.md) | GET | Retrieves tickets for a Billetweb event. |

