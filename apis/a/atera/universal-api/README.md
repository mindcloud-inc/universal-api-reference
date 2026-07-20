# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-16-at-16_1773689174304.png" alt="Atera logo" width="28" height="28"> Atera: Universal API

Monitor endpoints, manage tickets, customers, contacts, and alerts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/atera/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.atera.com
- **Vendor API docs:** https://app.atera.com/apidocs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get account info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get account info](actions/get-account-info.md) | GET | Retrieves account details from Atera. |

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Find agents](actions/find-agents.md) | GET | Finds agents in Atera. |
| [Find agents for customer](actions/find-agents-for-customer.md) | GET | Finds agents in Atera for a specific customer. |
| [Get agent](actions/get-agent.md) | GET | Retrieves an agent from Atera by ID. |

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Create alert](actions/create-alert.md) | POST | Creates an alert in Atera. |
| [Find alerts](actions/find-alerts.md) | GET | Finds alerts in Atera. |
| [Get alert](actions/get-alert.md) | GET | Retrieves an alert from Atera by ID. |
| [Resolve alert](actions/resolve-alert.md) | PUT | Updates an existing alert in Atera as resolved. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create contact](actions/create-contact.md) | POST | Creates a contact in Atera. |
| [Find contacts](actions/find-contacts.md) | GET | Finds contacts in Atera. |
| [Get contact](actions/get-contact.md) | GET | Retrieves a contact from Atera by ID. |
| [Update contact](actions/update-contact.md) | PUT | Updates an existing contact in Atera. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create customer](actions/create-customer.md) | POST | Creates a customer in Atera. |
| [Find customers](actions/find-customers.md) | GET | Finds customers in Atera. |
| [Get customer](actions/get-customer.md) | GET | Retrieves a customer from Atera by ID. |
| [Update customer](actions/update-customer.md) | PUT | Updates an existing customer in Atera. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create ticket](actions/create-ticket.md) | POST | Creates a ticket in Atera. |
| [Find modified tickets](actions/find-modified-tickets.md) | GET | Finds recently modified tickets in Atera. |
| [Find tickets](actions/find-tickets.md) | GET | Finds tickets in Atera. |
| [Get ticket](actions/get-ticket.md) | GET | Retrieves a ticket from Atera by ID. |
| [Update ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in Atera. |

### Ticket Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Find ticket attachments](actions/find-ticket-attachments.md) | GET | Finds attachments for a specific Atera ticket. |

### Ticket Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add ticket comment](actions/add-ticket-comment.md) | POST | Creates a comment on a specific Atera ticket. |
| [Find ticket comments](actions/find-ticket-comments.md) | GET | Finds comments for a specific Atera ticket. |

