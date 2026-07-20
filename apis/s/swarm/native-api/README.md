# Swarm: Native API Reference

A consolidated summary of Swarm's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.theswarm.com/docs/api-reference/introduction
- **API base URL:** `https://bee.theswarm.com`

## Authentication

### API Key

Use a Swarm team API key from Team Settings > API. The key is sent in the x-api-key header for every request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.theswarm.com/docs/getting-started/quickstart)

## Pagination

Use `limit` in the request body to set the page size (default 25; accepted range 1–1000). Use `paginationToken` in the request body as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Companies](actions/fetch-companies.md) | `POST /companies/fetch` | [docs](https://docs.theswarm.com/docs/endpoints/fetch-company) |
| [Fetch Profiles](actions/fetch-profiles.md) | `POST /v2/profiles/fetch` | [docs](https://docs.theswarm.com/docs/endpoints/fetch-profile) |
| [Find Warm Paths by Company Name](actions/find-warm-paths-by-company-name.md) | `POST /v2/profiles/network-mapper` | [docs](https://docs.theswarm.com/docs/endpoints/network-mapper) |
| [Find Warm Paths by Company Website](actions/find-warm-paths-by-company-website.md) | `POST /v2/profiles/network-mapper` | [docs](https://docs.theswarm.com/docs/endpoints/network-mapper) |
| [Find Warm Paths by LinkedIn URL](actions/find-warm-paths-by-linkedin-url.md) | `POST /v2/profiles/network-mapper` | [docs](https://docs.theswarm.com/docs/endpoints/network-mapper) |
| [Get Post Comments](actions/get-post-comments.md) | `GET /social/post/:postUrn/comments` | [docs](https://docs.theswarm.com/docs/on-demand/get-comments) |
| [Get Post Reactions](actions/get-post-reactions.md) | `GET /social/post/:postUrn/reactions` | [docs](https://docs.theswarm.com/docs/on-demand/get-reactions) |
| [Get Post Reshares](actions/get-post-reshares.md) | `GET /social/post/:postUrn/reshares` | [docs](https://docs.theswarm.com/docs/on-demand/get-reshares) |
| [Get Profile Posts](actions/get-profile-posts.md) | `GET /social/profile/posts` | [docs](https://docs.theswarm.com/docs/on-demand/get-posts) |
| [Refresh Profile](actions/refresh-profile.md) | `GET /v2/profiles/fetch/refresh` | [docs](https://docs.theswarm.com/docs/on-demand/refresh-profile) |
| [Search Companies](actions/search-companies.md) | `POST /companies/search` | [docs](https://docs.theswarm.com/docs/endpoints/search-companies) |
| [Search Profiles](actions/search-profiles.md) | `POST /v2/profiles/search` | [docs](https://docs.theswarm.com/docs/endpoints/search-profiles) |
