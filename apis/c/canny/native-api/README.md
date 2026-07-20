# Canny: Native API Reference

A consolidated summary of Canny's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.canny.io/api-reference
- **API base URL:** `https://canny.io/api`

## Authentication

### API Key

Use a Canny secret API key from your company settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.canny.io/api-reference#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Post Category](actions/change-post-category.md) | `POST /v1/posts/change_category` | [docs](https://developers.canny.io/api-reference#change_post_category) |
| [Change Post Status](actions/change-post-status.md) | `POST /v1/posts/change_status` | [docs](https://developers.canny.io/api-reference#change_post_status) |
| [Create Category](actions/create-category.md) | `POST /v1/categories/create` | [docs](https://developers.canny.io/api-reference#create_category) |
| [Create Comment](actions/create-comment.md) | `POST /v1/comments/create` | [docs](https://developers.canny.io/api-reference#create_comment) |
| [Create Entry](actions/create-entry.md) | `POST /v1/entries/create` | [docs](https://developers.canny.io/api-reference#create_entry) |
| [Create or Update User](actions/create-or-update-user.md) | `POST /v1/users/create_or_update` | [docs](https://developers.canny.io/api-reference#create_or_update_user) |
| [Create Post](actions/create-post.md) | `POST /v1/posts/create` | [docs](https://developers.canny.io/api-reference#create_post) |
| [Create Tag](actions/create-tag.md) | `POST /v1/tags/create` | [docs](https://developers.canny.io/api-reference#create_tag) |
| [List Boards](actions/list-boards.md) | `POST /v1/boards/list` | [docs](https://developers.canny.io/api-reference#list_all_boards) |
| [List Categories](actions/list-categories.md) | `POST /v1/categories/list` | [docs](https://developers.canny.io/api-reference#list_categories) |
| [List Comments](actions/list-comments.md) | `POST /v1/comments/list` | [docs](https://developers.canny.io/api-reference#list_comments) |
| [List Companies](actions/list-companies.md) | `POST /v2/companies/list` | [docs](https://developers.canny.io/api-reference#list_companies) |
| [List Entries](actions/list-entries.md) | `POST /v1/entries/list` | [docs](https://developers.canny.io/api-reference#list_entries) |
| [List Ideas](actions/list-ideas.md) | `POST /v1/ideas/list` | [docs](https://developers.canny.io/api-reference#list_ideas) |
| [List Posts](actions/list-posts.md) | `POST /v1/posts/list` | [docs](https://developers.canny.io/api-reference#list_posts) |
| [List Tags](actions/list-tags.md) | `POST /v1/tags/list` | [docs](https://developers.canny.io/api-reference#list_tags) |
| [List Users](actions/list-users.md) | `POST /v2/users/list` | [docs](https://developers.canny.io/api-reference#list_users) |
| [Merge Idea](actions/merge-idea.md) | `POST /v1/ideas/merge` | [docs](https://developers.canny.io/api-reference#merge_idea) |
| [Retrieve Board](actions/retrieve-board.md) | `POST /v1/boards/retrieve` | [docs](https://developers.canny.io/api-reference#retrieve_board) |
| [Retrieve Idea](actions/retrieve-idea.md) | `POST /v1/ideas/retrieve` | [docs](https://developers.canny.io/api-reference#retrieve_idea) |
| [Retrieve Post](actions/retrieve-post.md) | `POST /v1/posts/retrieve` | [docs](https://developers.canny.io/api-reference#retrieve_post) |
| [Retrieve User](actions/retrieve-user.md) | `POST /v1/users/retrieve` | [docs](https://developers.canny.io/api-reference#retrieve_user) |
| [Update Company](actions/update-company.md) | `POST /v1/companies/update` | [docs](https://developers.canny.io/api-reference#update_company) |
| [Update Post](actions/update-post.md) | `POST /v1/posts/update` | [docs](https://developers.canny.io/api-reference#update_post) |
