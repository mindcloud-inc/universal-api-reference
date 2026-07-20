# Usedesk: Native API Reference

A consolidated summary of Usedesk's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.usedocs.com/
- **API base URL:** `https://secure.usedesk.com/uapi`

## Authentication

### API Key

Authenticate with a Usedesk API channel secret key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.usedocs.com/article/51373)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Article Rating](actions/add-article-rating.md) | `POST /support/:account_id/articles/:id/change-rating` | [docs](https://api.usedocs.com/article/51402) |
| [Add Article Views](actions/add-article-views.md) | `POST /support/:account_id/articles/:id/add-views` | [docs](https://api.usedocs.com/article/51401) |
| [Change Chat Assignee](actions/change-chat-assignee.md) | `POST /chat/changeAssignee` | [docs](https://api.usedocs.com/article/51396) |
| [Create Agent](actions/create-agent.md) | `POST /create/user` | [docs](https://api.usedocs.com/article/51415) |
| [Create Chat](actions/create-chat.md) | `POST /chat/addMessage` | [docs](https://api.usedocs.com/article/51394) |
| [Create Client](actions/create-client.md) | `POST /create/client` | [docs](https://api.usedocs.com/article/51385) |
| [Create Comment](actions/create-comment.md) | `POST /create/comment` | [docs](https://api.usedocs.com/article/51381) |
| [Create Ticket](actions/create-ticket.md) | `POST /create/ticket` | [docs](https://api.usedocs.com/article/51378) |
| [Get Article](actions/get-article.md) | `GET /support/:account_id/articles/:id` | [docs](https://api.usedocs.com/article/51400) |
| [Get Client](actions/get-client.md) | `POST /client` | [docs](https://api.usedocs.com/article/51384) |
| [Get Ticket](actions/get-ticket.md) | `POST /ticket` | [docs](https://api.usedocs.com/article/51377) |
| [List Additional Fields](actions/list-additional-fields.md) | `POST /ticket/fields` | [docs](https://api.usedocs.com/article/51411) |
| [List Agent Groups](actions/list-agent-groups.md) | `POST /groups` | [docs](https://api.usedocs.com/article/51418) |
| [List Agents](actions/list-agents.md) | `POST /users` | [docs](https://api.usedocs.com/article/51414) |
| [List Articles](actions/list-articles.md) | `GET /support/:account_id/articles/list` | [docs](https://api.usedocs.com/article/51399) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://api.usedocs.com/article/51397) |
| [List Clients](actions/list-clients.md) | `POST /clients` | [docs](https://api.usedocs.com/article/51383) |
| [List Knowledge Base Structure](actions/list-knowledge-base-structure.md) | `GET /support/:account_id/list` | [docs](https://api.usedocs.com/article/51398) |
| [List Tags](actions/list-tags.md) | `POST /tags` | [docs](https://api.usedocs.com/article/51382) |
| [List Tickets](actions/list-tickets.md) | `POST /tickets` | [docs](https://api.usedocs.com/article/51376) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /chat/sendMessage` | [docs](https://api.usedocs.com/article/51395) |
| [Update Agent](actions/update-agent.md) | `POST /update/user` | [docs](https://api.usedocs.com/article/51416) |
| [Update Client](actions/update-client.md) | `POST /update/client` | [docs](https://api.usedocs.com/article/51386) |
| [Update Ticket](actions/update-ticket.md) | `POST /update/ticket` | [docs](https://api.usedocs.com/article/51379) |
