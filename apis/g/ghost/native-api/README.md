# Ghost: Native API Reference

A consolidated summary of Ghost's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.ghost.org/
- **API base URL:** `{adminDomain}/ghost/api/admin`

## Authentication

### Admin Integration Token

Ghost Admin API keys contain an ID and hexadecimal secret separated by a colon. Split the key, sign a short-lived HS256 JWT with the decoded secret, and send the token with the `Ghost` authorization scheme. Generate tokens only in trusted server-side code.

### Credentials

- **Site URL:** `adminDomain` · required · Your Ghost site origin, for example https://your-site.ghost.io
- **Admin API Key:** `adminApiKey` · required · Your Ghost Custom Integration Admin API key in id:secret format.

Send these headers with each API request:

```http
Authorization: Ghost <jwt>
```

```js
import jwt from 'jsonwebtoken';

const [id, secret] = adminApiKey.split(':');
const token = jwt.sign({}, Buffer.from(secret, 'hex'), {
  algorithm: 'HS256',
  audience: '/admin/',
  expiresIn: '5m',
  keyid: id
});

const response = await fetch(url, {
  headers: {
    Authorization: `Ghost ${token}`
  }
});
```

[Official authentication documentation](https://docs.ghost.org/admin-api#token-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept-Version` | `v6.0` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `posts`. The total page count is read from `meta.pagination.pages`. The current page number is read from `meta.pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 15). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Page](actions/copy-page.md) | `POST /pages/:id/copy` | [docs](https://docs.ghost.org/admin-api/pages/overview) |
| [Create Member](actions/create-member.md) | `POST /members/` | [docs](https://docs.ghost.org/admin-api/members/creating-a-member) |
| [Create Newsletter](actions/create-newsletter.md) | `POST /newsletters/` | [docs](https://docs.ghost.org/admin-api/newsletters/creating-a-newsletter) |
| [Create Offer](actions/create-offer.md) | `POST /offers/` | [docs](https://docs.ghost.org/admin-api/offers/creating-an-offer) |
| [Create Page](actions/create-page.md) | `POST /pages/` | [docs](https://docs.ghost.org/admin-api/pages/overview) |
| [Create Post](actions/create-post.md) | `POST /posts/` | [docs](https://docs.ghost.org/admin-api/posts/creating-a-post) |
| [Create Tier](actions/create-tier.md) | `POST /tiers/` | [docs](https://docs.ghost.org/admin-api/tiers/creating-a-tier) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/` | [docs](https://docs.ghost.org/admin-api/webhooks/creating-a-webhook) |
| [Delete Page](actions/delete-page.md) | `DELETE /pages/:id/` | [docs](https://docs.ghost.org/admin-api/pages/overview) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/:id/` | [docs](https://docs.ghost.org/admin-api/posts/deleting-a-post) |
| [Get Page by ID](actions/get-page-by-id.md) | `GET /pages/:id/` | [docs](https://docs.ghost.org/admin-api/pages/overview) |
| [Get Post by ID](actions/get-post-by-id.md) | `GET /posts/:id/` | [docs](https://docs.ghost.org/admin-api/posts/overview) |
| [Get Post by Slug](actions/get-post-by-slug.md) | `GET /posts/slug/:slug/` | [docs](https://docs.ghost.org/admin-api/posts/overview) |
| [List Members](actions/list-members.md) | `GET /members/` | [docs](https://docs.ghost.org/admin-api/members/overview) |
| [List Newsletters](actions/list-newsletters.md) | `GET /newsletters/` | [docs](https://docs.ghost.org/admin-api/newsletters/overview) |
| [List Offers](actions/list-offers.md) | `GET /offers/` | [docs](https://docs.ghost.org/admin-api/offers/overview) |
| [List Pages](actions/list-pages.md) | `GET /pages/` | [docs](https://docs.ghost.org/admin-api/pages/overview) |
| [List Posts](actions/list-posts.md) | `GET /posts/` | [docs](https://docs.ghost.org/admin-api/posts/overview) |
| [List Tiers](actions/list-tiers.md) | `GET /tiers/` | [docs](https://docs.ghost.org/admin-api/tiers/overview) |
| [Publish Post](actions/publish-post.md) | `PUT /posts/:id/` | [docs](https://docs.ghost.org/admin-api/posts/publishing-a-post) |
| [Schedule Post](actions/schedule-post.md) | `PUT /posts/:id/` | [docs](https://docs.ghost.org/admin-api/posts/scheduling-a-post) |
| [Update Member](actions/update-member.md) | `PUT /members/:id/` | [docs](https://docs.ghost.org/admin-api/members/updating-a-member) |
| [Update Newsletter](actions/update-newsletter.md) | `PUT /newsletters/:id/` | [docs](https://docs.ghost.org/admin-api/newsletters/updating-a-newsletter) |
| [Update Offer](actions/update-offer.md) | `PUT /offers/:id/` | [docs](https://docs.ghost.org/admin-api/offers/updating-an-offer) |
| [Update Page](actions/update-page.md) | `PUT /pages/:id/` | [docs](https://docs.ghost.org/admin-api/pages/overview) |
| [Update Post](actions/update-post.md) | `PUT /posts/:id/` | [docs](https://docs.ghost.org/admin-api/posts/updating-a-post) |
| [Update Tier](actions/update-tier.md) | `PUT /tiers/:id/` | [docs](https://docs.ghost.org/admin-api/tiers/updating-a-tier) |
| [Upload Image](actions/upload-image.md) | `POST /images/upload/` | [docs](https://docs.ghost.org/admin-api/images/uploading-an-image) |
