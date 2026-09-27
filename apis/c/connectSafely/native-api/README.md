# ConnectSafely: Native API Reference

A consolidated summary of ConnectSafely's API configuration and 97 documented operations, with links to official documentation.

- **Official docs:** https://connectsafely.ai/docs/api
- **API base URL:** `https://api.connectsafely.ai/linkedin`
- **OpenAPI specification:** https://connectsafely.ai/docs/api/openapi.yaml

## Authentication

### API key

ConnectSafely uses a single workspace API key, sent as a Bearer token.

1. Sign in to ConnectSafely and open [connectsafely.ai/api-key](https://connectsafely.ai/api-key).
2. Generate an API key and copy it.
3. Send it on every request as `Authorization: Bearer <YOUR_API_KEY>`.

[Official authentication documentation](https://connectsafely.ai/docs/api/overview)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Authorization` | `Bearer <YOUR_API_KEY>` |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Every endpoint acts through one of the LinkedIn accounts connected to the workspace. Pass `accountId` to choose one; omit it to use the workspace default.

Responses carry a `success` boolean. Failures return `success: false` with a stable `code` and a human-readable `message`:

```json
{
  "success": false,
  "code": "validation_error",
  "message": "Explanation of what went wrong"
}
```

## Rate limits

Two independent limits apply, and either can return `429` with `Retry-After` (seconds) plus `X-RateLimit-Limit`, `X-RateLimit-Remaining` and `X-RateLimit-Reset`:

- **Per API key:** 60 requests per minute, with short bursts up to 100 requests per 10 seconds.
- **Per LinkedIn account, per minute:** 30 for search, profile and content reads; 15 for writes (`/connect`, `/message`, `/posts/comment`, `/posts/react`); 10 for `/account/*`; unlimited for inbox reads.

Some actions also carry a LinkedIn-side quota — for example `POST /connect` allows 90 connection requests per week per account. Quotas are noted on each action page.

## Pagination

Use `count` to set the page size and `start` as the record offset, both 0-indexed. Read endpoints take them as query parameters; the `POST` search endpoints take them as JSON body fields.

## Endpoints (97 documented)

### Account

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get account activity history](actions/get-account-activity.md) | `GET /account/:accountId/activity` | [docs](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-activity-get-account-activity) |
| [Get account premium status](actions/get-account-premium-status.md) | `GET /account/:accountId/premium` | [docs](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-premium-get-account-premium-status) |
| [Get account status](actions/get-account-status.md) | `GET /account/status` | [docs](https://connectsafely.ai/docs/api/linkedin-account/get-account-status-get-account-status) |
| [Get specific account status](actions/get-account-status-by-id.md) | `GET /account/:accountId/status` | [docs](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-status-get-account-status-by-id) |
| [List connected LinkedIn accounts (lightweight + searchable)](actions/list-linkedin-accounts.md) | `GET /accounts` | [docs](https://connectsafely.ai/docs/api/linkedin-account/get-accounts-list-linkedin-accounts) |
| [Quota usage for one account](actions/get-account-quota.md) | `GET /account/:accountId/quota` | [docs](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-quota-get-account-quota) |

### Actions

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept or ignore a received invitation](actions/respond-to-received-invitation.md) | `POST /invitations/received/respond` | [docs](https://connectsafely.ai/docs/api/linkedin-actions/post-invitations-received-respond-respond-to-received-invitation) |
| [Follow or unfollow a LinkedIn profile](actions/follow-user.md) | `POST /follow` | [docs](https://connectsafely.ai/docs/api/linkedin-actions/post-follow-follow-user) |
| [Send a connection request](actions/send-connection-request.md) | `POST /connect` | [docs](https://connectsafely.ai/docs/api/linkedin-actions/post-connect-send-connection-request) |
| [Send a LinkedIn message](actions/send-message.md) | `POST /message` | [docs](https://connectsafely.ai/docs/api/linkedin-actions/post-message-send-message) |
| [Withdraw a sent connection invitation](actions/withdraw-invitation.md) | `POST /invitations/withdraw` | [docs](https://connectsafely.ai/docs/api/linkedin-actions/post-invitations-withdraw-withdraw-invitation) |

### Analytics

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get "Manage my network" counts](actions/get-network-summary.md) | `GET /analytics/network/summary` | [docs](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-network-summary-get-network-summary) |
| [Get creator dashboard overview](actions/get-creator-dashboard.md) | `GET /analytics/creator/dashboard` | [docs](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-creator-dashboard-get-creator-dashboard) |
| [Get exact connection count](actions/get-connection-count.md) | `GET /analytics/connections/count` | [docs](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-connections-count-get-connection-count) |
| [Get followers analytics](actions/get-followers-analytics.md) | `GET /analytics/followers` | [docs](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-followers-get-followers-analytics) |
| [List an account's own comments](actions/get-account-comments.md) | `GET /account/:accountId/comments` | [docs](https://connectsafely.ai/docs/api/linkedin-analytics/get-account-accountid-comments-get-account-comments) |
| [List an account's own reactions](actions/get-account-reactions.md) | `GET /account/:accountId/reactions` | [docs](https://connectsafely.ai/docs/api/linkedin-analytics/get-account-accountid-reactions-get-account-reactions) |

### Conversations

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check if a conversation exists with a profile](actions/conversation-exists.md) | `GET /conversations/exists/:profileId` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-exists-profileid-conversation-exists) |
| [Delete (recall) a message](actions/conversations-delete-message.md) | `DELETE /conversations/:conversationUrn/messages/:messageUrn` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/delete-conversations-conversationurn-messages-messageurn-conversations-delete-message) |
| [Download media from message](actions/conversations-download-media.md) | `POST /conversations/download-media` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-download-media-conversations-download-media) |
| [Get conversation messages](actions/get-conversation-messages.md) | `GET /conversations/:conversationUrn/messages` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-conversationurn-messages-get-conversation-messages) |
| [Get sync status](actions/conversations-sync-status.md) | `GET /conversations/sync/status` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-sync-status-conversations-sync-status) |
| [List conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-list-conversations) |
| [Mark a conversation as unread](actions/conversations-mark-unread.md) | `PATCH /conversations/:conversationUrn/mark-unread` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/patch-conversations-conversationurn-mark-unread-conversations-mark-unread) |
| [React or unreact to a message](actions/conversations-react-message.md) | `POST /conversations/:conversationUrn/messages/:messageUrn/react` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-conversationurn-messages-messageurn-react-conversations-react-message) |
| [Refresh conversation messages](actions/conversations-refresh.md) | `POST /conversations/refresh` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-refresh-conversations-refresh) |
| [Send message (with channel selection)](actions/conversations-send-message.md) | `POST /conversations/send` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-send-conversations-send-message) |
| [Star a conversation](actions/conversations-star.md) | `PATCH /conversations/:conversationUrn/star` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/patch-conversations-conversationurn-star-conversations-star) |
| [Trigger conversation sync](actions/conversations-sync.md) | `POST /conversations/sync` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-sync-conversations-sync) |
| [Unstar a conversation](actions/conversations-unstar.md) | `PATCH /conversations/:conversationUrn/unstar` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/patch-conversations-conversationurn-unstar-conversations-unstar) |
| [Upload message attachment](actions/conversations-upload-attachment.md) | `POST /conversations/upload-attachment` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-upload-attachment-conversations-upload-attachment) |

### Events

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get event attendees](actions/get-event-attendees.md) | `GET /events/:eventId/attendees` | [docs](https://connectsafely.ai/docs/api/uncategorized/get-events-eventid-attendees-get-event-attendees) |

### Groups

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get group members (legacy endpoint)](actions/get-group-members-legacy.md) | `POST /group-members` | [docs](https://connectsafely.ai/docs/api/linkedin-groups/post-group-members-get-group-members-legacy) |
| [Get group members by group ID](actions/get-group-members.md) | `POST /groups/members` | [docs](https://connectsafely.ai/docs/api/linkedin-groups/post-groups-members-get-group-members) |
| [Get group members by group URL](actions/get-group-members-by-url.md) | `POST /groups/members-by-url` | [docs](https://connectsafely.ai/docs/api/linkedin-groups/post-groups-members-by-url-get-group-members-by-url) |

### InMail

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get InMail credits](actions/get-inmail-credits.md) | `GET /inmail/credits` | [docs](https://connectsafely.ai/docs/api/uncategorized/get-inmail-credits-get-inmail-credits) |

### Messaging

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check if profile supports email messaging](actions/check-email-support.md) | `POST /messaging/check-email-support` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-check-email-support-check-email-support) |
| [Get conversation details](actions/get-conversation-details.md) | `GET /messaging/conversation-details` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-messaging-conversation-details-get-conversation-details) |
| [Get recent messages](actions/get-recent-messages.md) | `GET /messaging/recent-messages` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-messaging-recent-messages-get-recent-messages) |
| [Mark all messages as read](actions/mark-all-messages-read.md) | `POST /messaging/mark-all-read` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-mark-all-read-mark-all-messages-read) |
| [Mark conversation as seen](actions/mark-conversation-seen.md) | `POST /messaging/mark-seen` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-mark-seen-mark-conversation-seen) |
| [Send a message (messaging wrapper)](actions/messaging-send.md) | `POST /messaging/send` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-messaging-send) |
| [Send group message with delivery acknowledgment](actions/send-group-message-with-ack.md) | `POST /messaging/send-group-with-ack` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-group-with-ack-send-group-message-with-ack) |
| [Send group message with typing indicator](actions/send-group-message-with-typing.md) | `POST /messaging/send-group-with-typing` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-group-with-typing-send-group-message-with-typing) |
| [Send message with delivery acknowledgment](actions/send-message-with-ack.md) | `POST /messaging/send-with-ack` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-with-ack-send-message-with-ack) |
| [Send message with group context](actions/send-group-message.md) | `POST /messaging/send-group` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-group-send-group-message) |
| [Send message with typing indicator](actions/send-message-with-typing.md) | `POST /messaging/send-with-typing` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-with-typing-send-message-with-typing) |
| [Send typing indicator](actions/send-typing-indicator.md) | `POST /messaging/typing-indicator` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-typing-indicator-send-typing-indicator) |

### Posts

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check document (PDF) processing status](actions/upload-document-status.md) | `GET /posts/upload/document-status` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/get-posts-upload-document-status-upload-document-status) |
| [Comment on a LinkedIn post](actions/comment-on-post.md) | `POST /posts/comment` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-comment-comment-on-post) |
| [Complete multipart video upload](actions/upload-complete.md) | `POST /posts/upload/complete` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-upload-complete-upload-complete) |
| [Create a LinkedIn post](actions/create-post.md) | `POST /posts/create` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-create-create-post) |
| [Get all comments from a post](actions/get-all-post-comments.md) | `POST /posts/comments/all` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-comments-all-get-all-post-comments) |
| [Get comments from a post](actions/get-post-comments.md) | `POST /posts/comments` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-comments-get-post-comments) |
| [Get latest posts from a profile](actions/get-latest-posts.md) | `POST /posts/latest` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-latest-get-latest-posts) |
| [Get reactions from a post](actions/get-post-reactions.md) | `POST /posts/reactions` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-reactions-get-post-reactions) |
| [Get reactions from a post (v2 - with vanity names)](actions/get-post-reactions-v2.md) | `POST /posts/reactions/v2` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-reactions-v2-get-post-reactions-v2) |
| [Get the current user's LinkedIn home feed](actions/get-feed.md) | `POST /feed` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-feed-get-feed) |
| [Get the list of people who reposted a post](actions/get-reposts.md) | `POST /posts/reposts` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-reposts-get-reposts) |
| [Initialize media upload — get pre-signed URL(s)](actions/upload-init.md) | `POST /posts/upload/init` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-upload-init-upload-init) |
| [Like a comment](actions/like-comment.md) | `POST /like-comment` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-like-comment-like-comment) |
| [React to a LinkedIn post](actions/react-to-post.md) | `POST /posts/react` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-react-react-to-post) |
| [Reply to a comment](actions/reply-to-comment.md) | `POST /reply` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-reply-reply-to-comment) |
| [Repost a LinkedIn post](actions/repost-post.md) | `POST /posts/repost` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-repost-repost-post) |
| [Scrape LinkedIn post details](actions/scrape-post.md) | `POST /posts/scrape` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-scrape-scrape-post) |
| [Search posts by keyword](actions/search-posts.md) | `POST /posts/search` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-search-search-posts) |
| [Upload media and create a LinkedIn post (server-side)](actions/upload-and-post.md) | `POST /posts/upload-and-post` | [docs](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-upload-and-post-upload-and-post) |

### Profile

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Endorse a skill on a LinkedIn profile](actions/endorse-skill.md) | `POST /endorse-skill` | [docs](https://connectsafely.ai/docs/api/linkedin-profiles/post-endorse-skill-endorse-skill) |
| [Fetch LinkedIn profile information](actions/fetch-profile.md) | `POST /profile` | [docs](https://connectsafely.ai/docs/api/linkedin-profiles/post-profile-fetch-profile) |
| [Fetch LinkedIn profile information (GET)](actions/get-profile.md) | `GET /profile` | [docs](https://connectsafely.ai/docs/api/linkedin-profiles/get-profile-get-profile) |
| [Get company/organization followers](actions/get-company-followers.md) | `GET /organizations/:companyId/followers` | [docs](https://connectsafely.ai/docs/api/linkedin-profiles/get-organizations-companyid-followers-get-company-followers) |
| [Send company follow invitations](actions/send-company-follow-invitations.md) | `POST /organizations/:companyId/follow-invitations` | [docs](https://connectsafely.ai/docs/api/linkedin-profiles/post-organizations-companyid-follow-invitations-send-company-follow-invitations) |

### Profiles

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Visit a LinkedIn profile](actions/visit-profile.md) | `POST /profile/visit` | [docs](https://connectsafely.ai/docs/api/linkedin-profiles/post-profile-visit-visit-profile) |

### Relationships

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check relationship status with profile](actions/check-relationship.md) | `GET /relationship/:profileId` | [docs](https://connectsafely.ai/docs/api/linkedin-actions/get-relationship-profileid-check-relationship) |
| [Check relationship status with specific account](actions/check-relationship-specific-account.md) | `GET /relationship/:accountId/:profileId` | [docs](https://connectsafely.ai/docs/api/linkedin-actions/get-relationship-accountid-profileid-check-relationship-specific-account) |

### Sales Navigator

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Sales Navigator thread with messages](actions/sales-nav-get-thread.md) | `GET /sales-nav/threads/:threadId` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-sales-nav-threads-threadid-sales-nav-get-thread) |
| [List Sales Navigator threads](actions/sales-nav-list-threads.md) | `GET /sales-nav/threads` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/get-sales-nav-threads-sales-nav-list-threads) |
| [Mark Sales Navigator thread as read](actions/sales-nav-mark-read.md) | `POST /sales-nav/mark-read` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-sales-nav-mark-read-sales-nav-mark-read) |
| [Send Sales Navigator message](actions/sales-nav-send-message.md) | `POST /sales-nav/send` | [docs](https://connectsafely.ai/docs/api/linkedin-messaging/post-sales-nav-send-sales-nav-send-message) |

### Search

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get company details](actions/get-company-details.md) | `POST /search/companies/details` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-companies-details-get-company-details) |
| [Get group details](actions/get-group-details.md) | `POST /search/groups/details` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-groups-details-get-group-details) |
| [Get job details](actions/get-job-details.md) | `POST /search/jobs/details` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-jobs-details-get-job-details) |
| [Search geo locations](actions/search-geo-locations.md) | `POST /search/geo` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-geo-search-geo-locations) |
| [Search LinkedIn companies](actions/search-companies.md) | `POST /search/companies` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-companies-search-companies) |
| [Search LinkedIn groups](actions/search-groups.md) | `POST /search/groups` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-groups-search-groups) |
| [Search LinkedIn jobs](actions/search-jobs.md) | `POST /search/jobs` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-jobs-search-jobs) |
| [Search LinkedIn people](actions/search-people.md) | `POST /search/people` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-people-search-people) |
| [Search LinkedIn people (alias)](actions/search-people-alias.md) | `POST /people/search` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-people-search-search-people-alias) |
| [Search LinkedIn people (V2 - with auto-pagination)](actions/search-people-v2.md) | `POST /search/people/v2` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-people-v2-search-people-v2) |
| [Search LinkedIn posts (V2 - with auto-pagination)](actions/search-posts-v2.md) | `POST /search/posts/v2` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-posts-v2-search-posts-v2) |
| [Search schools](actions/search-schools.md) | `POST /search/schools` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-schools-search-schools) |
| [Search service categories](actions/search-service-categories.md) | `POST /search/service-categories` | [docs](https://connectsafely.ai/docs/api/linkedin-search/post-search-service-categories-search-service-categories) |

### User

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get connections list](actions/get-connections.md) | `GET /connections` | [docs](https://connectsafely.ai/docs/api/linkedin-user/get-connections-get-connections) |
| [Get profile visitors](actions/get-profile-visitors.md) | `POST /profile/visitors` | [docs](https://connectsafely.ai/docs/api/linkedin-user/post-profile-visitors-get-profile-visitors) |
| [Get received invitations](actions/get-received-invitations.md) | `GET /invitations/received` | [docs](https://connectsafely.ai/docs/api/linkedin-user/get-invitations-received-get-received-invitations) |
| [Get sent connection invitations](actions/get-sent-invitations.md) | `GET /invitations/sent` | [docs](https://connectsafely.ai/docs/api/linkedin-user/get-invitations-sent-get-sent-invitations) |
| [Get user organizations](actions/get-organizations.md) | `GET /organizations` | [docs](https://connectsafely.ai/docs/api/linkedin-user/get-organizations-get-organizations) |
