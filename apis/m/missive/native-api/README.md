# Missive: Native API Reference

A consolidated summary of Missive's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://missiveapp.com/docs/developers/rest-api
- **API base URL:** `https://public.missiveapp.com/v1`

## Authentication

### API Key

Connect Missive with a personal API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://missiveapp.com/docs/developers/rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Draft](actions/create-draft.md) | `POST /drafts` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-draft) |
| [Create Incoming Message](actions/create-incoming-message.md) | `POST /messages` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-message) |
| [Create Post](actions/create-post.md) | `POST /posts` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-post) |
| [Create Response](actions/create-response.md) | `POST /responses` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#create-response-s) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-task) |
| [Delete Draft](actions/delete-draft.md) | `DELETE /drafts/:id` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#delete-a-draft) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/:id` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#delete-a-post) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:id` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#get-a-conversation) |
| [Get Message](actions/get-message.md) | `GET /messages/:id` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#get-a-message) |
| [Get Response](actions/get-response.md) | `GET /responses/:id` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#get-a-response) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#get-a-task) |
| [List Contact Books](actions/list-contact-books.md) | `GET /contact_books` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-contact-books) |
| [List Conversation Comments](actions/list-conversation-comments.md) | `GET /conversations/:id/comments` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversation-comments) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /conversations/:id/messages` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversation-messages) |
| [List Conversation Posts](actions/list-conversation-posts.md) | `GET /conversations/:id/posts` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversation-posts) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversations) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-organizations) |
| [List Responses](actions/list-responses.md) | `GET /responses` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-responses) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-tasks) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-teams) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-users) |
| [Merge Conversations](actions/merge-conversations.md) | `POST /conversations/:id/merge` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#merge-conversations) |
| [Search Messages by Email Message ID](actions/search-messages-by-email-message-id.md) | `GET /messages` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#list-messages) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id` | [docs](https://missiveapp.com/docs/developers/rest-api/endpoints#update-a-task) |
