# ProductLift: Native API Reference

A consolidated summary of ProductLift's API configuration and 75 documented operations, with links to official documentation.

- **Official docs:** https://developer.productlift.dev/api/documentation/
- **OpenAPI specification:** https://app.productlift.dev/api/documentation/openapi.yaml
- **API base URL:** `https://mindcloud.productlift.dev/api/v1`

## Authentication

### API Key

Authenticate ProductLift API requests with a bearer API key from the portal API & Webhooks settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.productlift.dev/api/documentation/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (75 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | `POST /groups/{group}/users/{user}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Adjust Post Text](actions/adjust-post-text.md) | `POST /posts/{key}/adjust` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Approve Moderation Item](actions/approve-moderation-item.md) | `POST /moderation/approve/{type}/{id}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Bulk Block Users](actions/bulk-block-users.md) | `POST /users/bulk-block` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Bulk Delete Users](actions/bulk-delete-users.md) | `POST /users/bulk-delete` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Bulk Unblock Users](actions/bulk-unblock-users.md) | `POST /users/bulk-unblock` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create Category](actions/create-category.md) | `POST /categories` | [docs](https://developer.productlift.dev/api/documentation/#categories-POSTapi-v1-categories) |
| [Create Comment](actions/create-comment.md) | `POST /posts/{postId}/comments` | [docs](https://developer.productlift.dev/api/documentation/#comments-POSTapi-v1-posts--postId--comments) |
| [Create Feedback](actions/create-feedback.md) | `POST /feedback` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create Or Update Product Vision](actions/create-or-update-product-vision.md) | `POST /product-vision` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create Post](actions/create-post.md) | `POST /posts` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create Section](actions/create-section.md) | `POST /sections` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create Status](actions/create-status.md) | `POST /statuses` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/{id}` | [docs](https://developer.productlift.dev/api/documentation/#categories-DELETEapi-v1-categories--id) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /posts/{postId}/comments/{comment}` | [docs](https://developer.productlift.dev/api/documentation/#comments-DELETEapi-v1-posts--postId--comments--comment) |
| [Delete Feedback](actions/delete-feedback.md) | `DELETE /feedback/{id}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/{group}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/{key}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete Product Vision](actions/delete-product-vision.md) | `DELETE /product-vision` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete Section](actions/delete-section.md) | `DELETE /sections/{section}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete Status](actions/delete-status.md) | `DELETE /statuses/{status}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/{tag}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Delete User](actions/delete-user.md) | `DELETE /users/{user}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Find User By Email](actions/find-user-by-email.md) | `GET /users/find_by_email` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Generate Product Vision](actions/generate-product-vision.md) | `POST /product-vision/generate` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Get Group](actions/get-group.md) | `GET /groups/{group}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Get Portal](actions/get-portal.md) | `GET /portal` | [docs](https://developer.productlift.dev/api/documentation/#portal-GETapi-v1-portal) |
| [Get Post](actions/get-post.md) | `GET /posts/{key}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Get Product Vision](actions/get-product-vision.md) | `GET /product-vision` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Get Tab](actions/get-tab.md) | `GET /tabs/{tab}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Get User](actions/get-user.md) | `GET /users/{user}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Get Widget](actions/get-widget.md) | `GET /widgets/{widget}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Improve Post Writing](actions/improve-post-writing.md) | `POST /posts/{key}/improve` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://developer.productlift.dev/api/documentation/#categories-GETapi-v1-categories) |
| [List Child Sections](actions/list-child-sections.md) | `GET /sections/{section}/children` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Comments](actions/list-comments.md) | `GET /posts/{postId}/comments` | [docs](https://developer.productlift.dev/api/documentation/#comments-GETapi-v1-posts--postId--comments) |
| [List Feedback](actions/list-feedback.md) | `GET /feedback` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Group Users](actions/list-group-users.md) | `GET /groups/{group}/users` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Pending Moderation Items](actions/list-pending-moderation-items.md) | `GET /moderation/pending` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Post Votes](actions/list-post-votes.md) | `GET /posts/{postId}/votes` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Posts For Tab](actions/list-posts-for-tab.md) | `GET /posts/all` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Rejected Moderation Items](actions/list-rejected-moderation-items.md) | `GET /moderation/rejected` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Root Sections](actions/list-root-sections.md) | `GET /sections` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Statuses](actions/list-statuses.md) | `GET /statuses` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Tabs](actions/list-tabs.md) | `GET /tabs` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List User Group Filters](actions/list-user-group-filters.md) | `GET /users/groups-filter` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List User Plan Types](actions/list-user-plan-types.md) | `GET /users/plan-types` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List User Segment Metadata Keys](actions/list-user-segment-metadata-keys.md) | `GET /users/segment-metadata-keys` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.productlift.dev/api/documentation/) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Reject Moderation Item](actions/reject-moderation-item.md) | `POST /moderation/reject/{type}/{id}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Remove User From Group](actions/remove-user-from-group.md) | `DELETE /groups/{group}/users/{user}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Revoke Anonymous Vote](actions/revoke-anonymous-vote.md) | `DELETE /posts/{key}/anonymous_votes/{anonymous_id}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Revoke User Vote](actions/revoke-user-vote.md) | `DELETE /posts/{postId}/votes/{user}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Search Duplicate Posts](actions/search-duplicate-posts.md) | `GET /posts/search_duplicates` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Search Posts Within Tab](actions/search-posts-within-tab.md) | `GET /posts/search` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Summarize Feedback](actions/summarize-feedback.md) | `POST /feedback/summarize` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Toggle Post Publish](actions/toggle-post-publish.md) | `PUT /posts/{key}/toggle-publish` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Update Category](actions/update-category.md) | `PATCH /categories/{id}` | [docs](https://developer.productlift.dev/api/documentation/#categories-PATCHapi-v1-categories--id) |
| [Update Comment](actions/update-comment.md) | `PATCH /posts/{postId}/comments/{comment}` | [docs](https://developer.productlift.dev/api/documentation/#comments-PATCHapi-v1-posts--postId--comments--comment) |
| [Update Feedback](actions/update-feedback.md) | `PATCH /feedback/{id}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Update Group](actions/update-group.md) | `PATCH /groups/{group}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Update Post](actions/update-post.md) | `PATCH /posts/{key}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Update Section](actions/update-section.md) | `PATCH /sections/{section}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Update Status](actions/update-status.md) | `PATCH /statuses/{status}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/{tag}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Update User](actions/update-user.md) | `PATCH /users/{user}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Vote Anonymously](actions/vote-anonymously.md) | `POST /posts/{key}/anonymous_votes/{anonymous_id}` | [docs](https://developer.productlift.dev/api/documentation/) |
| [Vote With User](actions/vote-with-user.md) | `POST /posts/{postId}/votes/{user}` | [docs](https://developer.productlift.dev/api/documentation/) |
