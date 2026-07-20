# Kit: Native API Reference

A consolidated summary of Kit's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.kit.com/api-reference/overview
- **OpenAPI specification:** https://developers.kit.com/api-reference/v4.json
- **API base URL:** `https://api.kit.com/v4`

## Authentication

### OAuth 2.0

OAuth 2.0 authorization code flow for Kit.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.kit.com/v4/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.kit.com/v4/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.kit.com/v4/oauth/token.

[Official authentication documentation](https://developers.kit.com/api-reference/oauth-refresh-token-flow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 500; accepted range 1–1000). Use `after` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber to Form](actions/add-subscriber-to-form.md) | `POST /forms/:form_id/subscribers` | [docs](https://developers.kit.com/api-reference/forms/add-subscriber-to-form-by-email-address) |
| [Add Subscriber to Sequence](actions/add-subscriber-to-sequence.md) | `POST /sequences/:sequence_id/subscribers` | [docs](https://developers.kit.com/api-reference/sequences/add-subscriber-to-sequence-by-email-address) |
| [Add Tag to Subscriber](actions/add-tag-to-subscriber.md) | `POST /tags/:tag_id/subscribers/:id` | [docs](https://developers.kit.com/api-reference/tags/tag-a-subscriber) |
| [Create Broadcast](actions/create-broadcast.md) | `POST /broadcasts` | [docs](https://developers.kit.com/api-reference/broadcasts/create-a-broadcast) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom_fields` | [docs](https://developers.kit.com/api-reference/custom-fields/create-a-custom-field) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /subscribers` | [docs](https://developers.kit.com/api-reference/subscribers/create-a-subscriber) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://developers.kit.com/api-reference/tags/create-a-tag) |
| [Get Broadcast](actions/get-broadcast.md) | `GET /broadcasts/:id` | [docs](https://developers.kit.com/api-reference/broadcasts/get-a-broadcast) |
| [Get Current Account](actions/get-current-account.md) | `GET /account` | [docs](https://developers.kit.com/api-reference/accounts/get-current-account) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:id` | [docs](https://developers.kit.com/api-reference/subscribers/get-a-subscriber) |
| [List Broadcasts](actions/list-broadcasts.md) | `GET /broadcasts` | [docs](https://developers.kit.com/api-reference/broadcasts/list-broadcasts) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom_fields` | [docs](https://developers.kit.com/api-reference/custom-fields/list-custom-fields) |
| [List Form Subscribers](actions/list-form-subscribers.md) | `GET /forms/:form_id/subscribers` | [docs](https://developers.kit.com/api-reference/forms/list-subscribers-for-a-form) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://developers.kit.com/api-reference/forms/list-forms) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://developers.kit.com/api-reference/segments/list-segments) |
| [List Sequence Subscribers](actions/list-sequence-subscribers.md) | `GET /sequences/:sequence_id/subscribers` | [docs](https://developers.kit.com/api-reference/sequences/list-subscribers-for-a-sequence) |
| [List Sequences](actions/list-sequences.md) | `GET /sequences` | [docs](https://developers.kit.com/api-reference/sequences/list-sequences) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://developers.kit.com/api-reference/subscribers/list-subscribers) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developers.kit.com/api-reference/tags/list-tags) |
| [List Tags for Subscriber](actions/list-tags-for-subscriber.md) | `GET /subscribers/:subscriber_id/tags` | [docs](https://developers.kit.com/api-reference/subscribers/list-tags-for-a-subscriber) |
| [Remove Tag From Subscriber](actions/remove-tag-from-subscriber.md) | `DELETE /tags/:tag_id/subscribers/:id` | [docs](https://developers.kit.com/api-reference/tags/remove-tag-from-subscriber) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /subscribers/:id/unsubscribe` | [docs](https://developers.kit.com/api-reference/subscribers/unsubscribe-subscriber) |
| [Update Broadcast](actions/update-broadcast.md) | `PUT /broadcasts/:id` | [docs](https://developers.kit.com/api-reference/broadcasts/update-a-broadcast) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /subscribers/:id` | [docs](https://developers.kit.com/api-reference/subscribers/update-a-subscriber) |
