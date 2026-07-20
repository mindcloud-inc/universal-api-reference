# OneHash: Native API Reference

A consolidated summary of OneHash's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://developers.chatwoot.com/api-reference/introduction
- **OpenAPI specification:** https://raw.githubusercontent.com/chatwoot/chatwoot/develop/swagger/swagger.json
- **API base URL:** `https://chat.onehash.ai`

## Authentication

### Access Token

Use an agent access token from OneHash Chat profile settings. The runtime sends it as the api_access_token header on every request.

### Credentials

- **Access Token:** `accessToken` · optional · Agent access token from OneHash Chat profile settings.

[Official authentication documentation](https://developers.chatwoot.com/api-reference/account/get-account-details)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Labels](actions/add-contact-labels.md) | `POST /api/v1/accounts/:accountId/contacts/:id/labels` | [docs](https://developers.chatwoot.com/api-reference/contact-labels/add-labels) |
| [Add Conversation Labels](actions/add-conversation-labels.md) | `POST /api/v1/accounts/:accountId/conversations/:conversationId/labels` | [docs](https://developers.chatwoot.com/api-reference/conversations/add-labels) |
| [Assign Conversation](actions/assign-conversation.md) | `POST /api/v1/accounts/:accountId/conversations/:conversationId/assignments` | [docs](https://developers.chatwoot.com/api-reference/conversation-assignments/assign-conversation) |
| [Create Canned Response](actions/create-canned-response.md) | `POST /api/v1/accounts/:accountId/canned_responses` | [docs](https://developers.chatwoot.com/api-reference/canned-responses/add-a-new-canned-response) |
| [Create Contact](actions/create-contact.md) | `POST /api/v1/accounts/:accountId/contacts` | [docs](https://developers.chatwoot.com/api-reference/contacts/create-contact) |
| [Create Contact Inbox](actions/create-contact-inbox.md) | `POST /api/v1/accounts/:accountId/contacts/:id/contact_inboxes` | [docs](https://developers.chatwoot.com/api-reference/contacts/create-contact-inbox) |
| [Create Conversation](actions/create-conversation.md) | `POST /api/v1/accounts/:accountId/conversations` | [docs](https://developers.chatwoot.com/api-reference/conversations/create-new-conversation) |
| [Create Conversation Message](actions/create-conversation-message.md) | `POST /api/v1/accounts/:accountId/conversations/:conversationId/messages` | [docs](https://developers.chatwoot.com/api-reference/messages/create-new-message) |
| [Create Label](actions/create-label.md) | `POST /api/v1/accounts/:accountId/labels` | [docs](https://developers.chatwoot.com/api-reference/introduction) |
| [Delete Canned Response](actions/delete-canned-response.md) | `DELETE /api/v1/accounts/:accountId/canned_responses/:id` | [docs](https://developers.chatwoot.com/api-reference/canned-responses/remove-a-canned-response-from-account) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/v1/accounts/:accountId/contacts/:id` | [docs](https://developers.chatwoot.com/api-reference/contacts/delete-contact) |
| [Delete Label](actions/delete-label.md) | `DELETE /api/v1/accounts/:accountId/labels/:id` | [docs](https://developers.chatwoot.com/api-reference/introduction) |
| [Filter Contacts](actions/filter-contacts.md) | `POST /api/v1/accounts/:accountId/contacts/filter` | [docs](https://developers.chatwoot.com/api-reference/contacts/contact-filter) |
| [Filter Conversations](actions/filter-conversations.md) | `POST /api/v1/accounts/:accountId/conversations/filter` | [docs](https://developers.chatwoot.com/api-reference/conversations/conversations-filter) |
| [Get Account Details](actions/get-account-details.md) | `GET /api/v1/accounts/:accountId` | [docs](https://developers.chatwoot.com/api-reference/account/get-account-details) |
| [Get Contact](actions/get-contact.md) | `GET /api/v1/accounts/:accountId/contacts/:id` | [docs](https://developers.chatwoot.com/api-reference/contacts/show-contact) |
| [Get Conversation](actions/get-conversation.md) | `GET /api/v1/accounts/:accountId/conversations/:conversationId` | [docs](https://developers.chatwoot.com/api-reference/conversations/conversation-details) |
| [Get Conversation Counts](actions/get-conversation-counts.md) | `GET /api/v1/accounts/:accountId/conversations/meta` | [docs](https://developers.chatwoot.com/api-reference/conversations/get-conversation-counts) |
| [Get Conversation Reporting Events](actions/get-conversation-reporting-events.md) | `GET /api/v1/accounts/:accountId/conversations/:conversationId/reporting_events` | [docs](https://developers.chatwoot.com/api-reference/conversations/conversation-reporting-events) |
| [Get Label](actions/get-label.md) | `GET /api/v1/accounts/:accountId/labels/:id` | [docs](https://developers.chatwoot.com/api-reference/introduction) |
| [List Canned Responses](actions/list-canned-responses.md) | `GET /api/v1/accounts/:accountId/canned_responses` | [docs](https://developers.chatwoot.com/api-reference/canned-responses/list-all-canned-responses-in-an-account) |
| [List Contact Conversations](actions/list-contact-conversations.md) | `GET /api/v1/accounts/:accountId/contacts/:id/conversations` | [docs](https://developers.chatwoot.com/api-reference/contacts/contact-conversations) |
| [List Contact Labels](actions/list-contact-labels.md) | `GET /api/v1/accounts/:accountId/contacts/:id/labels` | [docs](https://developers.chatwoot.com/api-reference/contact-labels/list-labels) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v1/accounts/:accountId/contacts` | [docs](https://developers.chatwoot.com/api-reference/contacts/list-contacts) |
| [List Conversation Labels](actions/list-conversation-labels.md) | `GET /api/v1/accounts/:accountId/conversations/:conversationId/labels` | [docs](https://developers.chatwoot.com/api-reference/conversations/list-labels) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /api/v1/accounts/:accountId/conversations/:conversationId/messages` | [docs](https://developers.chatwoot.com/api-reference/messages/get-messages) |
| [List Conversations](actions/list-conversations.md) | `GET /api/v1/accounts/:accountId/conversations` | [docs](https://developers.chatwoot.com/api-reference/conversations/conversations-list) |
| [List Labels](actions/list-labels.md) | `GET /api/v1/accounts/:accountId/labels` | [docs](https://developers.chatwoot.com/api-reference/introduction) |
| [Search Contacts](actions/search-contacts.md) | `GET /api/v1/accounts/:accountId/contacts/search` | [docs](https://developers.chatwoot.com/api-reference/contacts/search-contacts) |
| [Toggle Conversation Priority](actions/toggle-conversation-priority.md) | `POST /api/v1/accounts/:accountId/conversations/:conversationId/toggle_priority` | [docs](https://developers.chatwoot.com/api-reference/conversations/toggle-priority) |
| [Toggle Conversation Status](actions/toggle-conversation-status.md) | `POST /api/v1/accounts/:accountId/conversations/:conversationId/toggle_status` | [docs](https://developers.chatwoot.com/api-reference/conversations/toggle-status) |
| [Toggle Conversation Typing Status](actions/toggle-conversation-typing-status.md) | `POST /api/v1/accounts/:accountId/conversations/:conversationId/toggle_typing_status` | [docs](https://developers.chatwoot.com/api-reference/conversations/toggle-typing-status) |
| [Update Canned Response](actions/update-canned-response.md) | `PATCH /api/v1/accounts/:accountId/canned_responses/:id` | [docs](https://developers.chatwoot.com/api-reference/canned-responses/update-canned-response-in-account) |
| [Update Contact](actions/update-contact.md) | `PUT /api/v1/accounts/:accountId/contacts/:id` | [docs](https://developers.chatwoot.com/api-reference/contacts/update-contact) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /api/v1/accounts/:accountId/conversations/:conversationId` | [docs](https://developers.chatwoot.com/api-reference/conversations/update-conversation) |
| [Update Conversation Custom Attributes](actions/update-conversation-custom-attributes.md) | `POST /api/v1/accounts/:accountId/conversations/:conversationId/custom_attributes` | [docs](https://developers.chatwoot.com/api-reference/conversations/update-custom-attributes) |
| [Update Label](actions/update-label.md) | `PATCH /api/v1/accounts/:accountId/labels/:id` | [docs](https://developers.chatwoot.com/api-reference/introduction) |
