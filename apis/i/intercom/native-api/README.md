# Intercom: Native API Reference

A consolidated summary of Intercom's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://developers.intercom.com/docs/references/introduction
- **OpenAPI specification:** https://developers.intercom.com/docs/references/2.14/rest-api/api.intercom.io.json
- **API base URL:** `https://api.intercom.io`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.intercom.com/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://api.intercom.io/auth/eagle/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `all`.

[Official authentication documentation](https://developers.intercom.com/docs/build-an-integration/learn-more/authentication/setting-up-oauth)

### Access Token

Use an Intercom Access Token to connect your own Intercom workspace for private integrations.

### Credentials

- **Access Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.intercom.com/building-apps/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pages.total_pages`. The current page number is read from `pages.page`.

## Pagination

Use `per_page` in the query string to set the page size (maximum 150). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Contact](actions/archive-contact.md) | `POST /contacts/:contact_id/archive` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/archivecontact) |
| [Attach Contact To Conversation](actions/attach-contact-to-conversation.md) | `POST /conversations/:conversation_id/customers` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/attachcontacttoconversation) |
| [Convert Conversation To Ticket](actions/convert-conversation-to-ticket.md) | `POST /conversations/:conversation_id/convert` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/convertconversationtoticket) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/createcontact) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/createconversation) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/createticket) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/deletecontact) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /conversations/:conversation_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/deleteconversation) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /tickets/:ticket_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/deleteticket) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/showcontact) |
| [Get Contact By External ID](actions/get-contact-by-external-id.md) | `GET /contacts/find_by_external_id/:external_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/showcontactbyexternalid) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:ticket_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/getticket) |
| [List Contact Companies](actions/list-contact-companies.md) | `GET /contacts/:contact_id/companies` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/listcompaniesforacontact) |
| [List Contact Segments](actions/list-contact-segments.md) | `GET /contacts/:contact_id/segments` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/listsegmentsforacontact) |
| [List Contact Subscriptions](actions/list-contact-subscriptions.md) | `GET /contacts/:contact_id/subscriptions` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/listsubscriptionsforacontact) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /contacts/:contact_id/tags` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/listtagsforacontact) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/listcontacts) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/listconversations) |
| [Manage Conversation Part](actions/manage-conversation.md) | `POST /conversations/:conversation_id/parts` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/manageconversation) |
| [Merge Contact](actions/merge-contact.md) | `POST /contacts/merge` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/mergecontact) |
| [Redact Conversation](actions/redact-conversation.md) | `POST /conversations/redact` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/redactconversation) |
| [Reply Conversation](actions/reply-conversation.md) | `POST /conversations/:conversation_id/reply` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/replyconversation) |
| [Reply Ticket](actions/reply-ticket.md) | `POST /tickets/:ticket_id/reply` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/replyticket) |
| [Retrieve Conversation](actions/retrieve-conversation.md) | `GET /conversations/:conversation_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/retrieveconversation) |
| [Search Contacts](actions/search-contacts.md) | `POST /contacts/search` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/searchcontacts) |
| [Search Conversations](actions/search-conversations.md) | `POST /conversations/search` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/searchconversations) |
| [Search Tickets](actions/search-tickets.md) | `POST /tickets/search` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/searchtickets) |
| [Unarchive Contact](actions/unarchive-contact.md) | `POST /contacts/:contact_id/unarchive` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/unarchivecontact) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/updatecontact) |
| [Update Conversation](actions/update-conversation.md) | `PUT /conversations/:conversation_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/updateconversation) |
| [Update Ticket](actions/update-ticket.md) | `PUT /tickets/:ticket_id` | [docs](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/updateticket) |
