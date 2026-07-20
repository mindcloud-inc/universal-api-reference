# Ayrshare: Native API Reference

A consolidated summary of Ayrshare's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.ayrshare.com/docs/apis/overview
- **API base URL:** `https://api.ayrshare.com/api`

## Authentication

### API Key

Use your Ayrshare API key from the Primary Profile in the Ayrshare dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ayrshare.com/docs/apis/overview#authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–1000).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add RSS Feed](actions/add-rss-feed.md) | `POST /feed` | [docs](https://www.ayrshare.com/docs/apis/feeds/add-feed) |
| [Analyze Post Sentiment](actions/analyze-post-sentiment.md) | `POST /generate/sentiment` | [docs](https://www.ayrshare.com/docs/apis/generate/sentiment) |
| [Check Banned Hashtag](actions/check-banned-hashtag.md) | `GET /hashtags/banned` | [docs](https://www.ayrshare.com/docs/apis/hashtags/check-hashtags) |
| [Check Post Length](actions/check-post-length.md) | `POST /post/checkPostWeight` | [docs](https://www.ayrshare.com/docs/apis/validate/check-post-length) |
| [Create Short Link](actions/create-short-link.md) | `POST /links` | [docs](https://www.ayrshare.com/docs/apis/links/create-short-link) |
| [Create User Profile](actions/create-user-profile.md) | `POST /profiles` | [docs](https://www.ayrshare.com/docs/apis/profiles/create-profile) |
| [Delete Post](actions/delete-post.md) | `DELETE /post` | [docs](https://www.ayrshare.com/docs/apis/post/delete-post) |
| [Delete RSS Feed](actions/delete-rss-feed.md) | `DELETE /feed` | [docs](https://www.ayrshare.com/docs/apis/feeds/delete-feed) |
| [Generate Auto Hashtags](actions/generate-auto-hashtags.md) | `POST /hashtags/auto` | [docs](https://www.ayrshare.com/docs/apis/hashtags/auto-hashtags) |
| [Generate Post Text](actions/generate-post-text.md) | `POST /generate/post` | [docs](https://www.ayrshare.com/docs/apis/generate/post-text) |
| [Generate Profile JWT](actions/generate-profile-jwt.md) | `POST /profiles/generateJWT` | [docs](https://www.ayrshare.com/docs/apis/profiles/generate-jwt) |
| [Get Link Analytics](actions/get-link-analytics.md) | `GET /links/:id` | [docs](https://www.ayrshare.com/docs/apis/links/link-analytics) |
| [Get Post](actions/get-post.md) | `GET /post/:id` | [docs](https://www.ayrshare.com/docs/apis/post/get-post) |
| [Get Post History By ID](actions/get-post-history-by-id.md) | `GET /history/:id` | [docs](https://www.ayrshare.com/docs/apis/history/get-history-id) |
| [Get User Profile Details](actions/get-user-profile-details.md) | `GET /user` | [docs](https://www.ayrshare.com/docs/apis/user/profile-details) |
| [List Media Gallery](actions/list-media-gallery.md) | `GET /media` | [docs](https://www.ayrshare.com/docs/apis/media/get-media-in-gallery) |
| [List Platform Post History](actions/list-platform-post-history.md) | `GET /history/:platform` | [docs](https://www.ayrshare.com/docs/apis/history/history-platform) |
| [List Post History](actions/list-post-history.md) | `GET /history` | [docs](https://www.ayrshare.com/docs/apis/history/get-history) |
| [List RSS Feeds](actions/list-rss-feeds.md) | `GET /feed` | [docs](https://www.ayrshare.com/docs/apis/feeds/get-feeds) |
| [List User Profiles](actions/list-user-profiles.md) | `GET /profiles` | [docs](https://www.ayrshare.com/docs/apis/profiles/get-profiles) |
| [Moderate Content](actions/moderate-content.md) | `POST /validate/moderation` | [docs](https://www.ayrshare.com/docs/apis/validate/moderation) |
| [Publish Post](actions/publish-post.md) | `POST /post` | [docs](https://www.ayrshare.com/docs/apis/post/post) |
| [Recommend Hashtags](actions/recommend-hashtags.md) | `GET /hashtags/recommend` | [docs](https://www.ayrshare.com/docs/apis/hashtags/recommend-hashtags) |
| [Rewrite Post](actions/rewrite-post.md) | `POST /generate/rewrite` | [docs](https://www.ayrshare.com/docs/apis/generate/rewrite-post) |
| [Search Hashtags](actions/search-hashtags.md) | `GET /hashtags/search` | [docs](https://www.ayrshare.com/docs/apis/hashtags/search-hashtags) |
| [Translate Post](actions/translate-post.md) | `POST /generate/translate` | [docs](https://www.ayrshare.com/docs/apis/generate/translate-post) |
| [Update RSS Feed](actions/update-rss-feed.md) | `PUT /feed` | [docs](https://www.ayrshare.com/docs/apis/feeds/update-feed) |
| [Update Scheduled Post](actions/update-scheduled-post.md) | `PATCH /post` | [docs](https://www.ayrshare.com/docs/apis/post/update-post) |
| [Update Short Link](actions/update-short-link.md) | `PUT /links/:id` | [docs](https://www.ayrshare.com/docs/apis/links/update-short-link) |
| [Update User Profile](actions/update-user-profile.md) | `PATCH /profiles` | [docs](https://www.ayrshare.com/docs/apis/profiles/update-profile) |
| [Validate Post](actions/validate-post.md) | `POST /validate/post` | [docs](https://www.ayrshare.com/docs/apis/validate/validate-post) |
| [Verify Media URL](actions/verify-media-url.md) | `POST /media/urlExists` | [docs](https://www.ayrshare.com/docs/apis/media/verify-media-url) |
