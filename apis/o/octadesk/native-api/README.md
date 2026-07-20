# Octadesk: Native API Reference

A consolidated summary of Octadesk's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developers.octadesk.com/reference
- **API base URL:** `{baseUrl}`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Agent Email:** `username` · required · Email associated with the Octadesk API key.
- **Base URL:** `baseUrl` · required · Account-specific Octadesk API base URL.

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
octa-agent-email: <username>
```

[Official authentication documentation](https://developers.octadesk.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | `GET /auth/check` | [docs](https://developers.octadesk.com/reference/checkapitoken) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.octadesk.com/reference/addcontact) |
| [Get Chat](actions/get-chat.md) | `GET /chat/:id` | [docs](https://developers.octadesk.com/reference/getchatbyid) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developers.octadesk.com/reference/getcontactbyid) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:number` | [docs](https://developers.octadesk.com/reference/getbynumber) |
| [List Chat Events](actions/list-chat-events.md) | `GET /chat/:id/events` | [docs](https://developers.octadesk.com/reference/geteventsbychatid) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /chat/:id/messages` | [docs](https://developers.octadesk.com/reference/getmessagesbychatid) |
| [List Chat Templates](actions/list-chat-templates.md) | `GET /chat/templates-message` | [docs](https://developers.octadesk.com/reference/gettemplatemessages) |
| [List Chats](actions/list-chats.md) | `GET /chat` | [docs](https://developers.octadesk.com/reference/getchatbyfilter) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.octadesk.com/reference/getall) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developers.octadesk.com/reference/getorganizations) |
| [List Survey Submissions](actions/list-survey-submissions.md) | `GET /survey/submissions` | [docs](https://developers.octadesk.com/reference/getsubmissions) |
| [List Ticket Channels](actions/list-ticket-channels.md) | `GET /tickets/channels` | [docs](https://developers.octadesk.com/reference/getchannels) |
| [List Ticket Forms](actions/list-ticket-forms.md) | `GET /tickets/forms` | [docs](https://developers.octadesk.com/reference/getforms) |
| [List Ticket Groups](actions/list-ticket-groups.md) | `GET /tickets/groups` | [docs](https://developers.octadesk.com/reference/getgroups) |
| [List Ticket Interactions](actions/list-ticket-interactions.md) | `GET /tickets/:number/interactions` | [docs](https://developers.octadesk.com/reference/getticketinteractions) |
| [List Ticket Priorities](actions/list-ticket-priorities.md) | `GET /tickets/priorities` | [docs](https://developers.octadesk.com/reference/getpriorities) |
| [List Ticket Statuses](actions/list-ticket-statuses.md) | `GET /tickets/status` | [docs](https://developers.octadesk.com/reference/getstatus) |
| [List Ticket Tags](actions/list-ticket-tags.md) | `GET /tickets/tags` | [docs](https://developers.octadesk.com/reference/gettags) |
| [List Ticket Types](actions/list-ticket-types.md) | `GET /tickets/types` | [docs](https://developers.octadesk.com/reference/gettypes) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://developers.octadesk.com/reference/getalltickets) |
| [List WhatsApp Numbers](actions/list-whatsapp-numbers.md) | `GET /chat/numbers` | [docs](https://developers.octadesk.com/reference/getnumbers) |
| [Replace Contact](actions/replace-contact.md) | `PUT /contacts/:id` | [docs](https://developers.octadesk.com/reference/updatecontactbyid) |
| [Search Ticket Interactions](actions/search-ticket-interactions.md) | `GET /tickets/interactions` | [docs](https://developers.octadesk.com/reference/searchallinteractions) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /chat/:id/messages` | [docs](https://developers.octadesk.com/reference/sendmessagetochat) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://developers.octadesk.com/reference/updatecontactinfobyid) |
