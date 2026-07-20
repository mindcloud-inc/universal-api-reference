# Hy.page: Native API Reference

A consolidated summary of Hy.page's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://platform.hyax.com/api-docs
- **API base URL:** `https://platform.hyax.com`

## Authentication

### API Key

Use a Hyax team API key to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.hyax.com/api-docs/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tags](actions/add-tags.md) | `POST /hyax-api/v1/people/tags/add` | [docs](https://platform.hyax.com/api-docs/people-tags-add) |
| [Archive Post](actions/archive-post.md) | `DELETE /hyax-api/v1/posts/:id` | [docs](https://platform.hyax.com/api-docs/post-delete) |
| [Book Meeting](actions/book-meeting.md) | `POST /hyax-api/v1/meetings/book` | [docs](https://platform.hyax.com/api-docs/meetings-book) |
| [Create or Update Person](actions/create-or-update-person.md) | `POST /hyax-api/v1/people/add` | [docs](https://platform.hyax.com/api-docs/people-add) |
| [Create Order](actions/create-order.md) | `POST /hyax-api/v1/orders` | [docs](https://platform.hyax.com/api-docs/order-create) |
| [Create Post](actions/create-post.md) | `POST /hyax-api/v1/posts` | [docs](https://platform.hyax.com/api-docs/post-create) |
| [Delete Person](actions/delete-person.md) | `DELETE /hyax-api/v1/people/:id` | [docs](https://platform.hyax.com/api-docs/people-delete) |
| [Enroll in Sequence](actions/enroll-in-sequence.md) | `POST /hyax-api/v1/sequences/enroll` | [docs](https://platform.hyax.com/api-docs/sequence-enroll) |
| [Get Order](actions/get-order.md) | `GET /hyax-api/v1/orders/:id` | [docs](https://platform.hyax.com/api-docs/order-get) |
| [Get Person by Email](actions/get-person-by-email.md) | `GET /hyax-api/v1/people/by-email` | [docs](https://platform.hyax.com/api-docs/people-by-email) |
| [Get Person by ID](actions/get-person-by-id.md) | `GET /hyax-api/v1/people/:id` | [docs](https://platform.hyax.com/api-docs/people-get) |
| [Get Post](actions/get-post.md) | `GET /hyax-api/v1/posts/:id` | [docs](https://platform.hyax.com/api-docs/post-get) |
| [Get Post Creation Job Status](actions/get-post-creation-job-status.md) | `GET /hyax-api/v1/posts/jobs/:id` | [docs](https://platform.hyax.com/api-docs/post-job-status) |
| [Get Product](actions/get-product.md) | `GET /hyax-api/v1/products/:id` | [docs](https://platform.hyax.com/api-docs/product-get) |
| [List Meeting Slots](actions/list-meeting-slots.md) | `GET /hyax-api/v1/meetings/slots` | [docs](https://platform.hyax.com/api-docs/meetings-slots) |
| [List Orders](actions/list-orders.md) | `GET /hyax-api/v1/orders` | [docs](https://platform.hyax.com/api-docs/orders-list) |
| [List People](actions/list-people.md) | `GET /hyax-api/v1/people` | [docs](https://platform.hyax.com/api-docs/people-list) |
| [List Posts](actions/list-posts.md) | `GET /hyax-api/v1/posts` | [docs](https://platform.hyax.com/api-docs/posts-list) |
| [List Products](actions/list-products.md) | `GET /hyax-api/v1/products` | [docs](https://platform.hyax.com/api-docs/products-list) |
| [List Touchpoints](actions/list-touchpoints.md) | `GET /hyax-api/v1/people/:id/touchpoints` | [docs](https://platform.hyax.com/api-docs/people-touchpoints) |
| [Remove Tags](actions/remove-tags.md) | `POST /hyax-api/v1/people/tags/remove` | [docs](https://platform.hyax.com/api-docs/people-tags-remove) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /hyax-api/v1/email/send` | [docs](https://platform.hyax.com/api-docs/email-send) |
| [Unsubscribe Person](actions/unsubscribe-person.md) | `POST /hyax-api/v1/people/unsubscribe` | [docs](https://platform.hyax.com/api-docs/people-unsubscribe) |
| [Update Post](actions/update-post.md) | `PATCH /hyax-api/v1/posts/:id` | [docs](https://platform.hyax.com/api-docs/post-patch) |
