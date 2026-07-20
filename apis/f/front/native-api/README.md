# Front: Native API Reference

A consolidated summary of Front's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://dev.frontapp.com/reference
- **OpenAPI specification:** https://raw.githubusercontent.com/frontapp/front-api-specs/main/core-api/core-api.json
- **API base URL:** `https://api2.frontapp.com`

## Authentication

### OAuth2

Connect Front using OAuth2 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.frontapp.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.frontapp.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `accounts:read accounts:write accounts:delete analytics:read attachments:read channels:read channels:write comments:read comments:write contacts:read contacts:write contacts:delete conversations:read conversations:write conversations:delete custom_fields:read drafts:read drafts:write drafts:delete events:read inboxes:read inboxes:write knowledge_bases:read knowledge_bases:write knowledge_bases:delete links:read links:write message_templates:read message_templates:write message_templates:delete messages:read messages:write messages:send rules:read shifts:read shifts:write signatures:read signatures:write signatures:delete statuses:read tags:read tags:write tags:delete teammate_groups:read teammate_groups:write teammate_groups:delete teammates:read teammates:write teams:read teams:write views:read views:write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.frontapp.com/oauth/token.

[Official authentication documentation](https://dev.frontapp.com/docs/oauth)

### API Key

Connect Front using a company-level API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.frontapp.com/docs/create-and-revoke-api-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `Pagination.next`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `page_token` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | `POST /conversations/:conversation_id/comments` | [docs](https://dev.frontapp.com/reference/add-comment) |
| [Add Conversation Followers](actions/add-conversation-followers.md) | `POST /conversations/:conversation_id/followers` | [docs](https://dev.frontapp.com/reference/add-conversation-followers) |
| [Add Conversation Tag](actions/add-conversation-tag.md) | `POST /conversations/:conversation_id/tags` | [docs](https://dev.frontapp.com/reference/add-conversation-tag) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://dev.frontapp.com/reference/create-contact) |
| [Create Draft Reply](actions/create-draft-reply.md) | `POST /conversations/:conversation_id/drafts` | [docs](https://dev.frontapp.com/reference/create-draft-reply) |
| [Delete Message Draft](actions/delete-message-draft.md) | `DELETE /drafts/:draft_id` | [docs](https://dev.frontapp.com/reference/delete-draft) |
| [Edit Message Draft](actions/edit-message-draft.md) | `PATCH /drafts/:message_id/` | [docs](https://dev.frontapp.com/reference/edit-draft) |
| [Get API Token Details](actions/get-api-token-details.md) | `GET /me` | [docs](https://dev.frontapp.com/reference/api-token-details) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:conversation_id` | [docs](https://dev.frontapp.com/reference/get-conversation-by-id) |
| [Get Message](actions/get-message.md) | `GET /messages/:message_id` | [docs](https://dev.frontapp.com/reference/get-message) |
| [Get Teammate](actions/get-teammate.md) | `GET /teammates/:teammate_id` | [docs](https://dev.frontapp.com/reference/get-teammate) |
| [List Assigned Conversations](actions/list-assigned-conversations.md) | `GET /teammates/:teammate_id/conversations` | [docs](https://dev.frontapp.com/reference/list-assigned-conversations) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://dev.frontapp.com/reference/list-channels) |
| [List Contact Conversations](actions/list-contact-conversations.md) | `GET /contacts/:contactId/conversations` | [docs](https://dev.frontapp.com/reference/list-contact-conversations) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /contacts/:contactId/notes` | [docs](https://dev.frontapp.com/reference/list-notes) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://dev.frontapp.com/reference/list-contacts) |
| [List Conversation Comments](actions/list-conversation-comments.md) | `GET /conversations/:conversation_id/comments` | [docs](https://dev.frontapp.com/reference/list-conversation-comments) |
| [List Conversation Drafts](actions/list-conversation-drafts.md) | `GET /conversations/:conversation_id/drafts` | [docs](https://dev.frontapp.com/reference/list-conversation-drafts) |
| [List Conversation Followers](actions/list-conversation-followers.md) | `GET /conversations/:conversation_id/followers` | [docs](https://dev.frontapp.com/reference/list-conversation-followers) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /conversations/:conversation_id/messages` | [docs](https://dev.frontapp.com/reference/list-conversation-messages) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://dev.frontapp.com/reference/list-conversations) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://dev.frontapp.com/reference/list-tags) |
| [List Teammates](actions/list-teammates.md) | `GET /teammates` | [docs](https://dev.frontapp.com/reference/list-teammates) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://dev.frontapp.com/reference/list-teams) |
| [List Views](actions/list-views.md) | `GET /views` | [docs](https://dev.frontapp.com/reference/list-views) |
| [Remove Conversation Tag](actions/remove-conversation-tag.md) | `DELETE /conversations/:conversation_id/tags` | [docs](https://dev.frontapp.com/reference/remove-conversation-tag) |
| [Search Conversations](actions/search-conversations.md) | `GET /conversations/search/:query` | [docs](https://dev.frontapp.com/reference/search-conversations) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:contact_id` | [docs](https://dev.frontapp.com/reference/update-a-contact) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /conversations/:conversation_id` | [docs](https://dev.frontapp.com/reference/update-conversation) |
| [Update Conversation Assignee](actions/update-conversation-assignee.md) | `PUT /conversations/:conversation_id/assignee` | [docs](https://dev.frontapp.com/reference/update-conversation-assignee) |
