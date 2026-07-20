# Mighty Networks: Native API Reference

A consolidated summary of Mighty Networks's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://docs.mightynetworks.com/admin-api
- **API base URL:** `https://api.mn.co/admin/v1`

## Authentication

### API Key

Authenticate with a Mighty Networks API key.

### Credentials

- **API Key:** `apiKey` · required
- **Network ID:** `networkId` · required · The Mighty Network ID or subdomain for this connection.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.mightynetworks.com/authentication)

## API conventions

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Space Member](actions/add-space-member.md) | `POST /networks/:network_id/spaces/:space_id/members` | [docs](https://docs.mightynetworks.com/api-reference/members/add-a-user-as-a-member-to-the-space) |
| [Archive Plan](actions/archive-plan.md) | `DELETE /networks/:network_id/plans/:id/` | [docs](https://docs.mightynetworks.com/api-reference/plans/archive-a-plan-this-will-cancel-all-associated-subscriptions-and-revoke-access) |
| [Create Event](actions/create-event.md) | `POST /networks/:network_id/events` | [docs](https://docs.mightynetworks.com/api-reference/events/creates-a-new-event-in-the-network) |
| [Create Post](actions/create-post.md) | `POST /networks/:network_id/posts` | [docs](https://docs.mightynetworks.com/api-reference/posts/create-a-new-post-and-optionally-notify-the-network) |
| [Create Post Comment](actions/create-post-comment.md) | `POST /networks/:network_id/posts/:post_id/comments` | [docs](https://docs.mightynetworks.com/api-reference/comments/create-a-new-comment-on-a-post) |
| [Create Space](actions/create-space.md) | `POST /networks/:network_id/spaces` | [docs](https://docs.mightynetworks.com/api-reference/spaces/create-a-new-space-in-the-network) |
| [Delete Event](actions/delete-event.md) | `DELETE /networks/:network_id/events/:id/` | [docs](https://docs.mightynetworks.com/api-reference/events/deletes-an-event) |
| [Delete Post](actions/delete-post.md) | `DELETE /networks/:network_id/posts/:id/` | [docs](https://docs.mightynetworks.com/api-reference/posts/delete-a-post-or-article) |
| [Delete Post Comment](actions/delete-post-comment.md) | `DELETE /networks/:network_id/posts/:post_id/comments/:id` | [docs](https://docs.mightynetworks.com/api-reference/comments/delete-a-comment-from-a-post) |
| [Delete Space](actions/delete-space.md) | `DELETE /networks/:network_id/spaces/:id` | [docs](https://docs.mightynetworks.com/api-reference/spaces/delete-a-space-by-its-id) |
| [Get Current User](actions/get-current-user.md) | `GET /networks/:network_id/me` | [docs](https://docs.mightynetworks.com/quickstart) |
| [Get Event](actions/get-event.md) | `GET /networks/:network_id/events/:id/` | [docs](https://docs.mightynetworks.com/api-reference/events/returns-details-of-a-specific-event) |
| [Get Network Member](actions/get-network-member.md) | `GET /networks/:network_id/members/:id/` | [docs](https://docs.mightynetworks.com/api-reference/members/return-a-single-member-by-id) |
| [Get Network Member by Email](actions/get-network-member-by-email.md) | `GET /networks/:network_id/members/by_email` | [docs](https://docs.mightynetworks.com/api-reference/members/return-a-single-member-by-email-address) |
| [Get Plan](actions/get-plan.md) | `GET /networks/:network_id/plans/:id/` | [docs](https://docs.mightynetworks.com/api-reference/plans/return-a-single-plan-by-id) |
| [Get Post](actions/get-post.md) | `GET /networks/:network_id/posts/:id/` | [docs](https://docs.mightynetworks.com/api-reference/posts/query-details-of-a-specific-post-by-its-id) |
| [Get Post Comment](actions/get-post-comment.md) | `GET /networks/:network_id/posts/:post_id/comments/:id` | [docs](https://docs.mightynetworks.com/api-reference/comments/query-details-of-a-specific-comment-by-its-id) |
| [Get Space](actions/get-space.md) | `GET /networks/:network_id/spaces/:id` | [docs](https://docs.mightynetworks.com/api-reference/spaces/query-details-of-a-specific-space-by-its-id) |
| [List Events](actions/list-events.md) | `GET /networks/:network_id/events` | [docs](https://docs.mightynetworks.com/api-reference/events/returns-a-paginated-list-of-events-in-the-network) |
| [List Network Members](actions/list-network-members.md) | `GET /networks/:network_id/members` | [docs](https://docs.mightynetworks.com/api-reference/members/return-members-of-the-given-network) |
| [List Plans](actions/list-plans.md) | `GET /networks/:network_id/plans` | [docs](https://docs.mightynetworks.com/api-reference/plans/return-all-plans-in-the-network) |
| [List Post Comments](actions/list-post-comments.md) | `GET /networks/:network_id/posts/:post_id/comments` | [docs](https://docs.mightynetworks.com/api-reference/comments/returns-a-list-of-comments-for-a-specific-post) |
| [List Posts](actions/list-posts.md) | `GET /networks/:network_id/posts` | [docs](https://docs.mightynetworks.com/api-reference/posts/returns-a-list-of-posts-for-the-current-network) |
| [List Space Members](actions/list-space-members.md) | `GET /networks/:network_id/spaces/:space_id/members` | [docs](https://docs.mightynetworks.com/api-reference/members/return-members-of-the-given-space) |
| [List Spaces](actions/list-spaces.md) | `GET /networks/:network_id/spaces` | [docs](https://docs.mightynetworks.com/api-reference/spaces/returns-a-list-of-spaces-for-the-current-network) |
| [Remove Space Member](actions/remove-space-member.md) | `DELETE /networks/:network_id/spaces/:space_id/members/:user_id/` | [docs](https://docs.mightynetworks.com/api-reference/members/remove-a-member-from-the-space) |
| [Update Network Member](actions/update-network-member.md) | `PATCH /networks/:network_id/members/:id/` | [docs](https://docs.mightynetworks.com/api-reference/members/update-a-members-role-in-the-network) |
| [Update Post](actions/update-post.md) | `PATCH /networks/:network_id/posts/:id/` | [docs](https://docs.mightynetworks.com/api-reference/posts/update-an-existing-post-or-article-1) |
| [Update Space](actions/update-space.md) | `PATCH /networks/:network_id/spaces/:id` | [docs](https://docs.mightynetworks.com/api-reference/spaces/update-a-space-by-its-id-1) |
