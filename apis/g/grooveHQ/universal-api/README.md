# <img src="https://images.mindcloud.co/apps/icons/apple-icon_1776273178341.png" alt="GrooveHQ logo" width="28" height="28"> GrooveHQ: Universal API

GrooveHQ customer support and help desk platform for tickets, messages, customers, agents, groups, and knowledge base content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grooveHQ/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.groovehq.com/
- **Vendor API docs:** https://doc.groovehq.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Search Knowledge Base Categories](actions/search-kb-categories.md) | GET | Searches knowledge base categories in GrooveHQ. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [List Mailboxes](actions/list-mailboxes.md) | GET | Retrieves mailboxes from GrooveHQ. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Knowledge Base](actions/get-knowledge-base.md) | GET | Retrieves a knowledge base from GrooveHQ. |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET | Retrieves knowledge bases from GrooveHQ. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from GrooveHQ by email. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from GrooveHQ. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in GrooveHQ. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from GrooveHQ. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from GrooveHQ. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Search Knowledge Base Articles](actions/search-kb-articles.md) | GET | Searches public knowledge base articles in GrooveHQ. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in a GrooveHQ ticket. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from GrooveHQ. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages for a ticket in GrooveHQ. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget](actions/get-widget.md) | GET | Retrieves a public widget from GrooveHQ. |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves widgets from GrooveHQ. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Counts](actions/list-ticket-counts.md) | GET | Retrieves ticket counts by folder from GrooveHQ. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Add Ticket Labels](actions/add-ticket-labels.md) | PUT | Adds labels to a ticket in GrooveHQ. |
| [Change Ticket Mailbox](actions/change-ticket-mailbox.md) | PUT | Changes a ticket's mailbox in GrooveHQ. |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in GrooveHQ. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from GrooveHQ. |
| [Get Ticket State](actions/get-ticket-state.md) | GET | Retrieves a ticket's state from GrooveHQ. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from GrooveHQ. |
| [Replace Ticket Labels](actions/replace-ticket-labels.md) | PUT | Replaces all labels on a ticket in GrooveHQ. |
| [Update Ticket Assignee](actions/update-ticket-assignee.md) | PUT | Updates a ticket's assignee in GrooveHQ. |
| [Update Ticket Group](actions/update-ticket-group.md) | PUT | Updates a ticket's assigned group in GrooveHQ. |
| [Update Ticket State](actions/update-ticket-state.md) | PUT | Updates a ticket's state in GrooveHQ. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from GrooveHQ by email. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from GrooveHQ. |
| [Get Ticket Assignee](actions/get-ticket-assignee.md) | GET | Retrieves a ticket's assignee from GrooveHQ. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from GrooveHQ. |

