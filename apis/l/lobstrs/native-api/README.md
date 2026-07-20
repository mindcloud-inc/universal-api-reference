# lobst.rs: Native API Reference

A consolidated summary of lobst.rs's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://lobste.rs/s/r9oskz/is_there_api_documentation_for_lobsters
- **API base URL:** `https://lobste.rs`

## Authentication

### No Authentication

The public Lobsters JSON page surface does not use authentication.

This API does not require request authentication.

[Official authentication documentation](https://lobste.rs/s/r9oskz/is_there_api_documentation_for_lobsters)

## API conventions

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Stories by URL](actions/find-stories-by-url.md) | `GET /stories/url/all.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [Get Comment](actions/get-comment.md) | `GET /c/:commentShortId.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [Get Story](actions/get-story.md) | `GET /s/:shortId.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [Get Story by Slug](actions/get-story-by-slug.md) | `GET /s/:shortId/:titleSlug.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [Get User Profile](actions/get-user-profile.md) | `GET /~:username.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [List Active Discussions](actions/list-active-discussions.md) | `GET /active.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [List Hottest Stories](actions/list-hottest-stories.md) | `GET /hottest.json` | [docs](https://lobste.rs/s/r9oskz/is_there_api_documentation_for_lobsters) |
| [List Newest Stories](actions/list-newest-stories.md) | `GET /newest.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [List Stories by Category](actions/list-stories-by-category.md) | `GET /categories/:category.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [List Stories by Domain](actions/list-stories-by-domain.md) | `GET /domains/:domain.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [List Stories by Tag](actions/list-stories-by-tag.md) | `GET /t/:tag.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [List Tags](actions/list-tags.md) | `GET /tags.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
| [List User Stories](actions/list-user-stories.md) | `GET /~:username/stories.json` | [docs](https://github.com/lobsters/lobsters/blob/main/config/routes.rb) |
