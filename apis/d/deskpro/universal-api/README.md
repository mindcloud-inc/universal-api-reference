# <img src="https://images.mindcloud.co/apps/icons/deskpro_1774641864444.png" alt="Deskpro logo" width="28" height="28"> Deskpro: Universal API

Deskpro is a help desk and customer support platform for tickets, users, organizations, knowledge content, and agent workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deskpro/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deskpro.com
- **Vendor API docs:** https://www.deskpro.com/developers/api-docs/v2.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Approvals

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Approvals](actions/list-ticket-approvals.md) | GET | Retrieves a list of ticket approvals from Deskpro. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Log](actions/get-ticket-log.md) | GET | Retrieves a ticket log from Deskpro. |
| [List Ticket Logs](actions/list-ticket-logs.md) | GET | Retrieves a list of ticket logs from Deskpro. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List Guides](actions/list-guides.md) | GET | Retrieves a list of guides from Deskpro. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Message](actions/get-ticket-message.md) | GET | Retrieves a ticket message from Deskpro. |
| [List Ticket Messages](actions/list-ticket-messages.md) | GET | Retrieves a list of ticket messages from Deskpro. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [List Articles](actions/list-articles.md) | GET | Retrieves a list of articles from Deskpro. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization record from Deskpro. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Deskpro. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket record from Deskpro. |
| [List Organization Tickets](actions/list-organization-tickets.md) | GET | Retrieves tickets for an organization in Deskpro. |
| [List Person Tickets](actions/list-person-tickets.md) | GET | Retrieves tickets for a person in Deskpro. |
| [List Ticket Filter Tickets](actions/list-ticket-filter-tickets.md) | GET | Retrieves tickets from a Deskpro ticket filter. |
| [List Ticket IDs](actions/list-ticket-ids.md) | GET | Retrieves a list of ticket IDs from Deskpro. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves a list of tickets from Deskpro. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent record from Deskpro. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Deskpro. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person record from Deskpro. |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of agents from Deskpro. |
| [List Online Agents](actions/list-online-agents.md) | GET | Retrieves a list of online agents from Deskpro. |
| [List People](actions/list-people.md) | GET | Retrieves a list of people from Deskpro. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Filter](actions/get-ticket-filter.md) | GET | Retrieves a ticket filter from Deskpro. |
| [Get Ticket Filter Count](actions/get-ticket-filter-count.md) | GET | Retrieves the ticket count for a Deskpro filter. |
| [List Ticket Filters](actions/list-ticket-filters.md) | GET | Retrieves a list of ticket filters from Deskpro. |

