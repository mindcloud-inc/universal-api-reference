# ChatBot: Native API Reference

A consolidated summary of ChatBot's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.chatbot.com/docs/
- **API base URL:** `https://api.chatbot.com`

## Authentication

### Developer Access Token

Use a ChatBot developer access token for Bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.chatbot.com/docs/)

## Pagination

Use `limit` in the query string to set the page size (default 40; accepted range 1–40). Use `after` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add segments to User](actions/add-segments-to-user.md) | `POST /users/:id/segments` | [docs](https://www.chatbot.com/docs/users/#add-segments-to-user) |
| [Ban or Unban User](actions/ban-or-unban-user.md) | `PUT /users/:id/ban` | [docs](https://www.chatbot.com/docs/users/#ban-or-unban-user) |
| [Create Segment](actions/create-segment.md) | `POST /users/segments` | [docs](https://www.chatbot.com/docs/users-segments/#create-segment) |
| [Create Story](actions/create-story.md) | `POST /v2/stories` | [docs](https://www.chatbot.com/docs/stories/#create-new-story) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://www.chatbot.com/docs/users/#create-user) |
| [Create User Entity](actions/create-user-entity.md) | `POST /entities` | [docs](https://www.chatbot.com/docs/user-entities/#add-new-entity) |
| [Export Users](actions/export-users.md) | `POST /users/export` | [docs](https://www.chatbot.com/docs/users/#export-users) |
| [Get Chat](actions/get-chat.md) | `GET /v2/chats/:chatId` | [docs](https://www.chatbot.com/docs/archives/#get-single-chat) |
| [Get Conversations Report](actions/get-conversations-report.md) | `GET /reports/conversations` | [docs](https://www.chatbot.com/docs/reports/#conversations-report) |
| [Get Story](actions/get-story.md) | `GET /v2/stories/:storyId` | [docs](https://www.chatbot.com/docs/stories/#list-single-story) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://www.chatbot.com/docs/users/#list-single-user) |
| [Get User Entity](actions/get-user-entity.md) | `GET /entities/:ID` | [docs](https://www.chatbot.com/docs/user-entities/#get-single-entity) |
| [List Chats](actions/list-chats.md) | `GET /v2/chats` | [docs](https://www.chatbot.com/docs/archives/#get-list-of-chats) |
| [List Phrases](actions/list-phrases.md) | `GET /training` | [docs](https://www.chatbot.com/docs/training/#list-all-phrases) |
| [List Segments](actions/list-segments.md) | `GET /users/segments` | [docs](https://www.chatbot.com/docs/users-segments/#list-all-segments) |
| [List Stories](actions/list-stories.md) | `GET /v2/stories` | [docs](https://www.chatbot.com/docs/stories/#list-all-stories) |
| [List User Entities](actions/list-user-entities.md) | `GET /entities` | [docs](https://www.chatbot.com/docs/user-entities/#list-all-user-entities) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.chatbot.com/docs/users/#list-all-users) |
| [Train Phrases](actions/train-phrases.md) | `PUT /training/train` | [docs](https://www.chatbot.com/docs/training/#train-phrases) |
| [Train with Custom Text](actions/train-with-custom-text.md) | `PUT /training/train/text` | [docs](https://www.chatbot.com/docs/training/#train-with-custom-text) |
| [Update Story](actions/update-story.md) | `PUT /v2/stories/:storyId` | [docs](https://www.chatbot.com/docs/stories/#update-existing-story) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://www.chatbot.com/docs/users/#update-user) |
| [Update User Entity](actions/update-user-entity.md) | `PUT /entities/:ID` | [docs](https://www.chatbot.com/docs/user-entities/#update-entity) |
| [Update User Segments](actions/update-user-segments.md) | `PUT /users/:id/segments` | [docs](https://www.chatbot.com/docs/users/#update-segments) |
