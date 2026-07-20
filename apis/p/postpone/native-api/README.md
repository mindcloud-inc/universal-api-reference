# Postpone: Native API Reference

A consolidated summary of Postpone's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.postpone.app/
- **API base URL:** `https://api.postpone.app`

## Authentication

### API Key

Authenticate with a personal Postpone API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.postpone.app/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Aggregate Post Metrics](actions/get-aggregate-post-metrics.md) | `POST /gql` | [docs](https://developers.postpone.app/analytics/aggregate-post-metrics) |
| [Get Aggregate Social Account Post Metrics](actions/get-aggregate-social-account-post-metrics.md) | `POST /gql` | [docs](https://developers.postpone.app/analytics/aggregate-social-account-post-metrics) |
| [Get Post Time Series Metrics](actions/get-post-time-series-metrics.md) | `POST /gql` | [docs](https://developers.postpone.app/analytics/post-time-series-metrics) |
| [Get Profile](actions/get-profile.md) | `POST /gql` | [docs](https://developers.postpone.app/examples/example-queries) |
| [List Bluesky Submissions](actions/list-bluesky-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [List Facebook Submissions](actions/list-facebook-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [List Instagram Submissions](actions/list-instagram-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [List LinkedIn Submissions](actions/list-linkedin-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [List Media](actions/list-media.md) | `POST /gql` | [docs](https://developers.postpone.app/examples/example-queries) |
| [List Next Schedule Dates](actions/list-next-schedule-dates.md) | `POST /gql` | [docs](https://developers.postpone.app/examples/example-queries) |
| [List Pinterest Submissions](actions/list-pinterest-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [List Post Tags](actions/list-post-tags.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/post-tags) |
| [List Reddit Submissions](actions/list-reddit-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [List Social Accounts](actions/list-social-accounts.md) | `POST /gql` | [docs](https://developers.postpone.app/examples/example-queries) |
| [List Threads Submissions](actions/list-threads-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [List Twitter Submissions](actions/list-twitter-submissions.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/retrieving-posts) |
| [Schedule Bluesky Post](actions/schedule-bluesky-post.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/bluesky) |
| [Schedule Facebook Post](actions/schedule-facebook-post.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/facebook) |
| [Schedule Instagram Post](actions/schedule-instagram-post.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/instagram) |
| [Schedule LinkedIn Post](actions/schedule-linkedin-post.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/linkedin) |
| [Schedule Pinterest Post](actions/schedule-pinterest-post.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/pinterest) |
| [Schedule Reddit Post](actions/schedule-reddit-post.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/reddit) |
| [Schedule Threads Post](actions/schedule-threads-post.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/threads) |
| [Schedule Tweet](actions/schedule-tweet.md) | `POST /gql` | [docs](https://developers.postpone.app/scheduling-posts/platforms/twitter) |
