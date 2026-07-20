# Website Toolbox Community: Native API Reference

A consolidated summary of Website Toolbox Community's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://www.websitetoolbox.com/docs/api/
- **API base URL:** `https://api.websitetoolbox.com/v1`

## Authentication

### API Key

Authenticate Website Toolbox API requests with an API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Website Toolbox secret API key from Integrate -> API.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.websitetoolbox.com/docs/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | `POST /api/categories` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Create Conversation](actions/create-conversation.md) | `POST /api/conversations` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Create Message](actions/create-message.md) | `POST /api/conversations/:conversationId/messages` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Create Moderator](actions/create-moderator.md) | `POST /api/category_moderators` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Create Post](actions/create-post.md) | `POST /api/posts` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Create Topic](actions/create-topic.md) | `POST /api/topics` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Create User Group](actions/create-user-group.md) | `POST /api/usergroups` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Delete Category](actions/delete-category.md) | `DELETE /api/categories/:categoryId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /api/conversations/:conversationId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Delete Moderator](actions/delete-moderator.md) | `DELETE /api/category_moderators/:moderatorId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Delete Post](actions/delete-post.md) | `DELETE /api/posts/:postId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Delete Topic](actions/delete-topic.md) | `DELETE /api/topics/:topicId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Get Category](actions/get-category.md) | `GET /api/categories/:categoryId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Get Conversation](actions/get-conversation.md) | `GET /api/conversations/:conversationId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Get Message](actions/get-message.md) | `GET /api/conversations/:conversationId/messages/:messageId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Get Moderator](actions/get-moderator.md) | `GET /api/category_moderators/:moderatorId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Get Post](actions/get-post.md) | `GET /api/posts/:postId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Get Topic](actions/get-topic.md) | `GET /api/topics/:topicId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Get User Group](actions/get-user-group.md) | `GET /api/usergroups/:usergroupId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Categories](actions/list-categories.md) | `GET /api/categories` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Category Permissions](actions/list-category-permissions.md) | `GET /api/categories/:categoryId/permissions` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Conversations](actions/list-conversations.md) | `GET /api/conversations` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Messages](actions/list-messages.md) | `GET /api/conversations/:conversationId/messages` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Moderators](actions/list-moderators.md) | `GET /api/category_moderators` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Page Views](actions/list-page-views.md) | `GET /api/page_views` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Posts](actions/list-posts.md) | `GET /api/posts` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Tags](actions/list-tags.md) | `GET /api/tags` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List Topics](actions/list-topics.md) | `GET /api/topics` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [List User Groups](actions/list-user-groups.md) | `GET /api/usergroups` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Update Category](actions/update-category.md) | `POST /api/categories/:categoryId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Update Category Permission](actions/update-category-permission.md) | `POST /api/categories/:categoryId/permissions/:userGroupId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Update Moderator](actions/update-moderator.md) | `POST /api/category_moderators/:moderatorId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Update Post](actions/update-post.md) | `POST /api/posts/:postId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Update Topic](actions/update-topic.md) | `POST /api/topics/:topicId` | [docs](https://www.websitetoolbox.com/docs/api/) |
| [Update User Group](actions/update-user-group.md) | `POST /api/usergroups/:usergroupId` | [docs](https://www.websitetoolbox.com/docs/api/) |
