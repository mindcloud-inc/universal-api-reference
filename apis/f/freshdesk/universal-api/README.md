# <img src="https://images.mindcloud.co/apps/icons/freshdesk_1773085268030.png" alt="Freshdesk logo" width="28" height="28"> Freshdesk: Universal API

Freshdesk: Manage tickets, contacts, and support conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freshdesk/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.freshworks.com/freshdesk/
- **Vendor API docs:** https://developers.freshdesk.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Currently Authenticated Agent](actions/get-currently-authenticated-agent.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-currently-authenticated-agent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from Freshdesk by ID. |
| [Get Currently Authenticated Agent](actions/get-currently-authenticated-agent.md) | GET | Retrieves the currently authenticated agent from Freshdesk. |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of agents from Freshdesk. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Freshdesk. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Freshdesk. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Freshdesk by ID. |
| [List Companies](actions/list-companies.md) | GET | Retrieves a list of companies from Freshdesk. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Freshdesk. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Freshdesk. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Freshdesk by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Freshdesk. |
| [Soft Delete a Contact](actions/soft-delete-a-contact.md) | DELETE | Deletes a contact from Freshdesk without permanently removing it. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Freshdesk. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a note on a Freshdesk ticket. |
| [Create Reply](actions/create-reply.md) | POST | Creates a reply to a Freshdesk ticket. |
| [List Ticket Conversations](actions/list-ticket-conversations.md) | GET | Retrieves ticket conversations from Freshdesk by ticket ID. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Freshdesk. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Freshdesk. |
| [Delete Ticket](actions/delete-ticket.md) | DELETE | Deletes an existing ticket from Freshdesk. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from Freshdesk by ID. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves a list of tickets from Freshdesk. |
| [Search Tickets](actions/search-tickets.md) | GET | Finds tickets in Freshdesk by query. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in Freshdesk. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Time Entries](actions/list-ticket-time-entries.md) | GET | Retrieves time entries for a Freshdesk ticket. |

