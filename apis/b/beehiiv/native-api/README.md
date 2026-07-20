# Beehiiv: Native API Reference

A consolidated summary of Beehiiv's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.beehiiv.com/api-reference/
- **OpenAPI specification:** https://files.buildwithfern.com/https%3A//beehiiv.docs.buildwithfern.com/d0f4c30b8707ec784c673704353550d3fb9e00a41983b8f2e3d852f96d93abdb/assets/beehiiv-API-Specification.yaml
- **API base URL:** `https://api.beehiiv.com`

## Authentication

### API Key Primary

Primary Beehiiv API key authentication using Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.beehiiv.com/welcome/create-an-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `total_pages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 350 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscription Tag](actions/add-subscription-tag.md) | `POST /v2/publications/:publicationId/subscriptions/:subscriptionId/tags` | [docs](https://developers.beehiiv.com/api-reference/subscription-tags/create) |
| [Bulk Create Subscriptions](actions/bulk-create-subscriptions.md) | `POST /v2/publications/:publicationId/bulk_subscriptions` | [docs](https://developers.beehiiv.com/api-reference/bulk-subscriptions/create) |
| [Create Publication Post](actions/create-publication-post.md) | `POST /v2/publications/:publicationId/posts` | [docs](https://developers.beehiiv.com/api-reference/posts/create) |
| [Create Publication Webhook](actions/create-publication-webhook.md) | `POST /v2/publications/:publicationId/webhooks` | [docs](https://developers.beehiiv.com/api-reference/webhooks/create) |
| [Create Subscription](actions/create-subscription.md) | `POST /v2/publications/:publicationId/subscriptions` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/create) |
| [Delete Publication Post](actions/delete-publication-post.md) | `DELETE /v2/publications/:publicationId/posts/:postId` | [docs](https://developers.beehiiv.com/api-reference/posts/delete) |
| [Delete Publication Webhook](actions/delete-publication-webhook.md) | `DELETE /v2/publications/:publicationId/webhooks/:endpointId` | [docs](https://developers.beehiiv.com/api-reference/webhooks/delete) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /v2/publications/:publicationId/subscriptions/:subscriptionId` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/delete) |
| [Get Bulk Subscription Update](actions/get-bulk-subscription-update.md) | `GET /v2/publications/:publicationId/bulk_subscription_updates/:id` | [docs](https://developers.beehiiv.com/api-reference/bulk-subscription-updates/show) |
| [Get Publication](actions/get-publication.md) | `GET /v2/publications/:publicationId` | [docs](https://developers.beehiiv.com/api-reference/publications/show) |
| [Get Publication Email Blast](actions/get-publication-email-blast.md) | `GET /v2/publications/:publicationId/email_blasts/:emailBlastId` | [docs](https://files.buildwithfern.com/https%3A//beehiiv.docs.buildwithfern.com/d0f4c30b8707ec784c673704353550d3fb9e00a41983b8f2e3d852f96d93abdb/assets/beehiiv-API-Specification.yaml) |
| [Get Publication Post](actions/get-publication-post.md) | `GET /v2/publications/:publicationId/posts/:postId` | [docs](https://developers.beehiiv.com/api-reference/posts/show) |
| [Get Publication Post Aggregate Stats](actions/get-publication-post-aggregate-stats.md) | `GET /v2/publications/:publicationId/posts/aggregate_stats` | [docs](https://developers.beehiiv.com/api-reference/posts/aggregate-stats) |
| [Get Publication Webhook](actions/get-publication-webhook.md) | `GET /v2/publications/:publicationId/webhooks/:endpointId` | [docs](https://developers.beehiiv.com/api-reference/webhooks/show) |
| [Get Subscription by Email](actions/get-subscription-by-email.md) | `GET /v2/publications/:publicationId/subscriptions/by_email/:email` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/get-by-email) |
| [Get Subscription by ID](actions/get-subscription-by-id.md) | `GET /v2/publications/:publicationId/subscriptions/:subscriptionId` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/get-by-id) |
| [Get Subscription by Subscriber ID](actions/get-subscription-by-subscriber-id.md) | `GET /v2/publications/:publicationId/subscriptions/by_subscriber_id/:subscriberId` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/index) |
| [Get Subscription JWT Token](actions/get-subscription-jwt-token.md) | `GET /v2/publications/:publicationId/subscriptions/:subscriptionId/jwt_token` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/index) |
| [Identify Workspace](actions/identify-workspace.md) | `GET /v2/workspaces/identify` | [docs](https://developers.beehiiv.com/api-reference/workspaces/identify) |
| [List Bulk Subscription Updates](actions/list-bulk-subscription-updates.md) | `GET /v2/publications/:publicationId/bulk_subscription_updates` | [docs](https://developers.beehiiv.com/api-reference/bulk-subscription-updates/index) |
| [List Publication Custom Fields](actions/list-publication-custom-fields.md) | `GET /v2/publications/:publicationId/custom_fields` | [docs](https://developers.beehiiv.com/api-reference/custom-fields/index) |
| [List Publication Email Blasts](actions/list-publication-email-blasts.md) | `GET /v2/publications/:publicationId/email_blasts` | [docs](https://files.buildwithfern.com/https%3A//beehiiv.docs.buildwithfern.com/d0f4c30b8707ec784c673704353550d3fb9e00a41983b8f2e3d852f96d93abdb/assets/beehiiv-API-Specification.yaml) |
| [List Publication Engagements](actions/list-publication-engagements.md) | `GET /v2/publications/:publicationId/engagements` | [docs](https://developers.beehiiv.com/api-reference/engagements/index) |
| [List Publication Posts](actions/list-publication-posts.md) | `GET /v2/publications/:publicationId/posts` | [docs](https://developers.beehiiv.com/api-reference/posts/index) |
| [List Publication Webhooks](actions/list-publication-webhooks.md) | `GET /v2/publications/:publicationId/webhooks` | [docs](https://developers.beehiiv.com/api-reference/webhooks/index) |
| [List Publications](actions/list-publications.md) | `GET /v2/publications` | [docs](https://developers.beehiiv.com/api-reference/publications/index) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v2/publications/:publicationId/subscriptions` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/index) |
| [Update Publication Webhook](actions/update-publication-webhook.md) | `PATCH /v2/publications/:publicationId/webhooks/:endpointId` | [docs](https://developers.beehiiv.com/api-reference/webhooks/update) |
| [Update Subscription by Email](actions/update-subscription-by-email.md) | `PUT /v2/publications/:publicationId/subscriptions/by_email/:email` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/update-by-email) |
| [Update Subscription by ID](actions/update-subscription-by-id.md) | `PATCH /v2/publications/:publicationId/subscriptions/:subscriptionId` | [docs](https://developers.beehiiv.com/api-reference/subscriptions/patch) |
