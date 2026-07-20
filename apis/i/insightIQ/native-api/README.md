# InsightIQ: Native API Reference

A consolidated summary of InsightIQ's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://docs.insightiq.ai/docs/api-reference/api
- **API base URL:** `{baseUrl}`

## Authentication

### Basic Authentication

Use your InsightIQ client ID as the username, your client secret as the password, and choose the target API environment.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Base URL:** `baseUrl` · required · Select the InsightIQ API environment base URL for this connection.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.insightiq.ai/docs/api-reference/api/ref)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Async Content Comments Fetch](actions/create-async-content-comments-fetch.md) | `POST /v1/social/creators/async/contents/comments/fetch` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Create Async Creator Profile Analytics](actions/create-async-creator-profile-analytics.md) | `POST /v1/social/creators/async/profiles/analytics` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Create Connection Link](actions/create-connection-link.md) | `POST /v1/links` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Create Media Safety Screening](actions/create-media-safety-screening.md) | `POST /v1/safety/media-screening` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Create SDK Token](actions/create-sdk-token.md) | `POST /v1/sdk-tokens` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Create User](actions/create-user.md) | `POST /v1/users` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Fetch Public Creator Content](actions/fetch-public-creator-content.md) | `POST /v1/social/creators/contents/fetch` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Async Content Comments Fetch](actions/get-async-content-comments-fetch.md) | `GET /v1/social/creators/async/contents/comments/fetch/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Async Creator Profile Analytics](actions/get-async-creator-profile-analytics.md) | `GET /v1/social/creators/async/profiles/analytics/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Creator Contact Info](actions/get-creator-contact-info.md) | `POST /v1/social/creators/profiles/contact-info` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Creator Profile Analytics](actions/get-creator-profile-analytics.md) | `POST /v1/social/creators/profiles/analytics` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Creator Topic Relevance](actions/get-creator-topic-relevance.md) | `GET /v1/social/creators/dictionary/topics/relevance` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Media Safety Screening](actions/get-media-safety-screening.md) | `GET /v1/safety/media-screening/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Trending Creators](actions/get-trending-creators.md) | `GET /v1/trends/creators` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Trending Hashtags](actions/get-trending-hashtags.md) | `GET /v1/trends/hashtag` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Trending Videos](actions/get-trending-videos.md) | `GET /v1/trends/videos` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get User](actions/get-user.md) | `GET /v1/users/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get User By External ID](actions/get-user-by-external-id.md) | `GET /v1/users/external_id/:external_id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Get Work Platform](actions/get-work-platform.md) | `GET /v1/work-platforms/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Creator Brands](actions/list-creator-brands.md) | `GET /v1/social/creators/dictionary/brands` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Creator Interests](actions/list-creator-interests.md) | `GET /v1/social/creators/dictionary/interests` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Creator Languages](actions/list-creator-languages.md) | `GET /v1/social/creators/dictionary/languages` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Creator Locations](actions/list-creator-locations.md) | `GET /v1/social/creators/dictionary/locations` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Flagging Criteria](actions/list-flagging-criteria.md) | `GET /v1/safety/flagging-criteria` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Professional Companies](actions/list-professional-companies.md) | `GET /v1/professional/creators/dictionary/companies` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Professional Education Degrees](actions/list-professional-education-degrees.md) | `GET /v1/professional/creators/dictionary/education-degrees` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Professional Education Institutes](actions/list-professional-education-institutes.md) | `GET /v1/professional/creators/dictionary/education-institutes` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Professional Locations](actions/list-professional-locations.md) | `GET /v1/professional/creators/dictionary/locations` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Professional Talks About](actions/list-professional-talks-about.md) | `GET /v1/professional/creators/dictionary/talks-about` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Professional Topics](actions/list-professional-topics.md) | `GET /v1/professional/creators/dictionary/topics` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Users](actions/list-users.md) | `GET /v1/users` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [List Work Platforms](actions/list-work-platforms.md) | `GET /v1/work-platforms` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Search Creator Topics](actions/search-creator-topics.md) | `GET /v1/social/creators/dictionary/topics` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
| [Update Webhook](actions/update-webhook.md) | `PUT /v1/webhooks/:id` | [docs](https://docs.insightiq.ai/docs/api-reference/api/ref) |
