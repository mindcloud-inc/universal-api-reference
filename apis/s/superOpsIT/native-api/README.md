# SuperOps IT: Native API Reference

A consolidated summary of SuperOps IT's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.superops.com/it
- **API base URL:** `https://api.superops.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Customer Subdomain:** `subdomain` · required · Your SuperOps tenant subdomain, the part before .superops.ai. For example, use mindcloud for https://mindcloud.superops.ai.

Send these headers with each API request:

```http
CustomerSubDomain: <subdomain>
```

[Official authentication documentation](https://support.superops.com/en/articles/6632215-how-to-integrate-applications-using-superops-ai-graphql-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `pageSize` in the request body to set the page size (maximum 100). Use `page` in the request body to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-createSite) |
| [Create Task](actions/create-task.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-createTask) |
| [Create Ticket](actions/create-ticket.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-createTicket) |
| [Create Ticket Conversation](actions/create-ticket-conversation.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-createTicketConversation) |
| [Create Ticket Note](actions/create-ticket-note.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-createTicketNote) |
| [Create User](actions/create-user.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-createUser) |
| [Get Asset](actions/get-asset.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getAsset) |
| [Get Asset Summary](actions/get-asset-summary.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getAssetSummary) |
| [Get Site](actions/get-site.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getSite) |
| [Get Task](actions/get-task.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getTask) |
| [Get Ticket](actions/get-ticket.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getTicket) |
| [Get User](actions/get-user.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getUser) |
| [List Asset Software](actions/list-asset-software.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getAssetSoftwareList) |
| [List Assets](actions/list-assets.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getAssetList) |
| [List Sites](actions/list-sites.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getSiteList) |
| [List Tasks](actions/list-tasks.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getTaskList) |
| [List Ticket Conversations](actions/list-ticket-conversations.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getTicketConversationList) |
| [List Ticket Notes](actions/list-ticket-notes.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getTicketNoteList) |
| [List Tickets](actions/list-tickets.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getTicketList) |
| [List Users](actions/list-users.md) | `POST /it` | [docs](https://developer.superops.com/it#query-getUserList) |
| [Update Asset](actions/update-asset.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-updateAsset) |
| [Update Site](actions/update-site.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-updateSite) |
| [Update Ticket](actions/update-ticket.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-updateTicket) |
| [Update User](actions/update-user.md) | `POST /it` | [docs](https://developer.superops.com/it#mutation-updateUser) |
