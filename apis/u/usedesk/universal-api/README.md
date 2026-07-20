# <img src="https://images.mindcloud.co/apps/icons/usedesk-png-icon_1775511235318.png" alt="Usedesk logo" width="28" height="28"> Usedesk: Universal API

Manage support tickets, clients, chats, and knowledge base

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/usedesk/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://usedesk.com
- **Vendor API docs:** https://api.usedocs.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Channels](actions/list-channels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Additional Field

| Action | Method | Description |
| --- | --- | --- |
| [List Additional Fields](actions/list-additional-fields.md) | GET | Retrieves a list of additional ticket fields from Usedesk. |

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Usedesk. |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of agents from Usedesk. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Usedesk. |

### Agent Group

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Groups](actions/list-agent-groups.md) | GET | Retrieves a list of agent groups from Usedesk. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Add Article Rating](actions/add-article-rating.md) | PUT | Adds a rating to a knowledge base article in Usedesk. |
| [Add Article Views](actions/add-article-views.md) | PUT | Adds views to a knowledge base article in Usedesk. |
| [Get Article](actions/get-article.md) | GET | Retrieves a knowledge base article by ID from Usedesk. |
| [List Articles](actions/list-articles.md) | GET | Retrieves a list of knowledge base articles from Usedesk. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves a list of channels from Usedesk. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Change Chat Assignee](actions/change-chat-assignee.md) | PUT | Updates a chat assignee in Usedesk. |
| [Create Chat](actions/create-chat.md) | POST | Creates a new chat in Usedesk. |
| [Send Chat Message](actions/send-chat-message.md) | POST | Sends a chat message in Usedesk. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Usedesk. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client by ID from Usedesk. |
| [List Clients](actions/list-clients.md) | GET | Retrieves a list of clients from Usedesk. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Usedesk. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new ticket comment in Usedesk. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [List Knowledge Base Structure](actions/list-knowledge-base-structure.md) | GET | Retrieves knowledge base directories and categories from Usedesk. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves a list of tags from Usedesk. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Usedesk. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket by ID from Usedesk. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves a list of tickets from Usedesk. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in Usedesk. |

