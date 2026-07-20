# Socialbu: Native API Reference

A consolidated summary of Socialbu's API configuration and 49 documented operations, with links to official documentation.

- **Official docs:** https://socialbu.com/developers/docs
- **OpenAPI specification:** https://socialbu.com/openapi.yaml
- **API base URL:** `https://socialbu.com/api/v1`

## Authentication

### API Key

Authenticate SocialBu API requests with a bearer API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://socialbu.com/developers/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (49 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Post to Queue](actions/add-post-to-queue.md) | `POST /queues/{id}/posts` | [docs](https://socialbu.com/developers/docs) |
| [Check Media Upload Status](actions/check-media-upload-status.md) | `GET /upload_media/status` | [docs](https://socialbu.com/developers/docs) |
| [Connect Account](actions/connect-account.md) | `POST /accounts` | [docs](https://socialbu.com/developers/docs) |
| [Create Post](actions/create-post.md) | `POST /posts` | [docs](https://socialbu.com/developers/docs) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://socialbu.com/developers/docs) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts/{accountId}` | [docs](https://socialbu.com/developers/docs) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/{postId}` | [docs](https://socialbu.com/developers/docs) |
| [Delete Team](actions/delete-team.md) | `DELETE /teams/{teamId}` | [docs](https://socialbu.com/developers/docs) |
| [Get Access Token](actions/get-access-token.md) | `POST /auth/get_token` | [docs](https://socialbu.com/developers/docs) |
| [Get Account](actions/get-account.md) | `GET /accounts/{accountId}` | [docs](https://socialbu.com/developers/docs) |
| [Get Accounts Metrics](actions/get-accounts-metrics.md) | `GET /insights/accounts/metrics` | [docs](https://socialbu.com/developers/docs) |
| [Get All Followers](actions/get-all-followers.md) | `GET /insights/accounts/followers` | [docs](https://socialbu.com/developers/docs) |
| [Get Automation Logs](actions/get-automation-logs.md) | `GET /insights/automations/logs` | [docs](https://socialbu.com/developers/docs) |
| [Get Curation Item](actions/get-curation-item.md) | `GET /curation/items/{id}` | [docs](https://socialbu.com/developers/docs) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://socialbu.com/developers/docs) |
| [Get Engagement Rate](actions/get-engagement-rate.md) | `GET /insights/accounts/engagement/rate` | [docs](https://socialbu.com/developers/docs) |
| [Get Engagement Trend](actions/get-engagement-trend.md) | `GET /insights/accounts/engagement/trend` | [docs](https://socialbu.com/developers/docs) |
| [Get Followers Growth](actions/get-followers-growth.md) | `GET /insights/accounts/followers/growth` | [docs](https://socialbu.com/developers/docs) |
| [Get Notification](actions/get-notification.md) | `GET /notifications/{id}` | [docs](https://socialbu.com/developers/docs) |
| [Get Open Conversations Count](actions/get-open-conversations-count.md) | `GET /insights/open-conversations-count` | [docs](https://socialbu.com/developers/docs) |
| [Get Post](actions/get-post.md) | `GET /posts/{postId}` | [docs](https://socialbu.com/developers/docs) |
| [Get Posts Counts](actions/get-posts-counts.md) | `GET /insights/posts/counts` | [docs](https://socialbu.com/developers/docs) |
| [Get Posts Metrics](actions/get-posts-metrics.md) | `GET /insights/posts/metrics` | [docs](https://socialbu.com/developers/docs) |
| [Get Supported Post Options](actions/get-supported-post-options.md) | `GET /posts/supported-options` | [docs](https://socialbu.com/developers/docs) |
| [Get Team Activity](actions/get-team-activity.md) | `GET /insights/teams/activity` | [docs](https://socialbu.com/developers/docs) |
| [Get Team Metrics](actions/get-team-metrics.md) | `GET /insights/teams/metrics` | [docs](https://socialbu.com/developers/docs) |
| [Get Top Posts](actions/get-top-posts.md) | `GET /insights/posts/top_posts` | [docs](https://socialbu.com/developers/docs) |
| [Get User Stats](actions/get-user-stats.md) | `GET /insights/stats` | [docs](https://socialbu.com/developers/docs) |
| [Initiate Media Upload](actions/initiate-media-upload.md) | `POST /upload_media` | [docs](https://socialbu.com/developers/docs) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://socialbu.com/developers/docs) |
| [List AI Tools](actions/list-ai-tools.md) | `GET /ai/tools` | [docs](https://socialbu.com/developers/docs) |
| [List Curation Items](actions/list-curation-items.md) | `GET /curation/items` | [docs](https://socialbu.com/developers/docs) |
| [List Curation Topics](actions/list-curation-topics.md) | `GET /curation/topics` | [docs](https://socialbu.com/developers/docs) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://socialbu.com/developers/docs) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://socialbu.com/developers/docs) |
| [List Queue Posts](actions/list-queue-posts.md) | `GET /queues/{id}/posts` | [docs](https://socialbu.com/developers/docs) |
| [List Queues](actions/list-queues.md) | `GET /queues` | [docs](https://socialbu.com/developers/docs) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://socialbu.com/developers/docs) |
| [List Unread Notifications](actions/list-unread-notifications.md) | `GET /notifications/unread` | [docs](https://socialbu.com/developers/docs) |
| [Logout](actions/logout.md) | `POST /auth/logout` | [docs](https://socialbu.com/developers/docs) |
| [Mark All Notifications as Read](actions/mark-all-notifications-as-read.md) | `POST /notifications/mark_all_read` | [docs](https://socialbu.com/developers/docs) |
| [Mark Notification as Read](actions/mark-notification-as-read.md) | `POST /notifications/{id}/mark_read` | [docs](https://socialbu.com/developers/docs) |
| [Mark Notification as Unread](actions/mark-notification-as-unread.md) | `POST /notifications/{id}/mark_unread` | [docs](https://socialbu.com/developers/docs) |
| [Run AI Tool](actions/run-ai-tool.md) | `POST /ai/tools/{slug}` | [docs](https://socialbu.com/developers/docs) |
| [Shuffle Queue](actions/shuffle-queue.md) | `POST /queues/{id}/shuffle` | [docs](https://socialbu.com/developers/docs) |
| [Update Account](actions/update-account.md) | `PATCH /accounts/{accountId}` | [docs](https://socialbu.com/developers/docs) |
| [Update Post](actions/update-post.md) | `PATCH /posts/{postId}` | [docs](https://socialbu.com/developers/docs) |
| [Update Team](actions/update-team.md) | `PUT /teams/{teamId}` | [docs](https://socialbu.com/developers/docs) |
| [Upload Media by URL](actions/upload-media-by-url.md) | `POST /upload_media_by_url` | [docs](https://socialbu.com/developers/docs) |
