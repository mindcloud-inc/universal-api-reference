# Tumblr: Native API Reference

A consolidated summary of Tumblr's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.tumblr.com/docs/en/api/v2
- **API base URL:** `https://api.tumblr.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.tumblr.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.tumblr.com/v2/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `basic write offline_access`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.tumblr.com/v2/oauth2/token.

[Official authentication documentation](https://www.tumblr.com/docs/en/api/v2#oauth2-authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Tumblr Integration` |

Response data is read from `response`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–20). Use `offset` in the query string as the record offset.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check If Blog Is Followed By Another Blog](actions/check-if-blog-is-followed-by-another-blog.md) | `GET /v2/blog/:blogIdentifier/followed_by` | [docs](https://www.tumblr.com/docs/en/api/v2#followed_by--check-if-followed-by-blog) |
| [Create Post (NPF)](actions/create-post-npf.md) | `POST /v2/blog/:blogIdentifier/posts` | [docs](https://www.tumblr.com/docs/en/api/v2#posts---createreblog-a-post-neue-post-format) |
| [Delete Post](actions/delete-post.md) | `POST /v2/blog/:blogIdentifier/post/delete` | [docs](https://www.tumblr.com/docs/en/api/v2#postdelete--delete-a-post) |
| [Follow Blog](actions/follow-blog.md) | `POST /v2/user/follow` | [docs](https://www.tumblr.com/docs/en/api/v2#userfollow--follow-a-blog) |
| [Get Blog Avatar](actions/get-blog-avatar.md) | `GET /v2/blog/:blogIdentifier/avatar/:size` | [docs](https://www.tumblr.com/docs/en/api/v2#avatar--retrieve-a-blog-avatar) |
| [Get Blog Info](actions/get-blog-info.md) | `GET /v2/blog/:blogIdentifier/info` | [docs](https://www.tumblr.com/docs/en/api/v2#info---retrieve-blog-info) |
| [Get Post Notes](actions/get-post-notes.md) | `GET /v2/blog/:blogIdentifier/notes` | [docs](https://www.tumblr.com/docs/en/api/v2#notes---get-notes-for-a-specific-post) |
| [Get Post (NPF)](actions/get-post-npf.md) | `GET /v2/blog/:blogIdentifier/posts/:postId` | [docs](https://www.tumblr.com/docs/en/api/v2#postspost-id---fetching-a-post-neue-post-format) |
| [Get Published Blog Posts](actions/get-published-blog-posts.md) | `GET /v2/blog/:blogIdentifier/posts` | [docs](https://www.tumblr.com/docs/en/api/v2#posts--retrieve-published-posts) |
| [Get User Dashboard](actions/get-user-dashboard.md) | `GET /v2/user/dashboard` | [docs](https://www.tumblr.com/docs/en/api/v2#userdashboard--retrieve-a-users-dashboard) |
| [Get User Information](actions/get-user-information.md) | `GET /v2/user/info` | [docs](https://www.tumblr.com/docs/en/api/v2#userinfo--get-a-users-information) |
| [Get User Limits](actions/get-user-limits.md) | `GET /v2/user/limits` | [docs](https://www.tumblr.com/docs/en/api/v2#userlimits--get-a-users-limits) |
| [Like Post](actions/like-post.md) | `POST /v2/user/like` | [docs](https://www.tumblr.com/docs/en/api/v2#userlike--like-a-post) |
| [List Blog Blocks](actions/list-blog-blocks.md) | `GET /v2/blog/:blogIdentifier/blocks` | [docs](https://www.tumblr.com/docs/en/api/v2#blocks--retrieve-blogs-blocks) |
| [List Blog Followers](actions/list-blog-followers.md) | `GET /v2/blog/:blogIdentifier/followers` | [docs](https://www.tumblr.com/docs/en/api/v2#followers--retrieve-a-blogs-followers) |
| [List Blog Following](actions/list-blog-following.md) | `GET /v2/blog/:blogIdentifier/following` | [docs](https://www.tumblr.com/docs/en/api/v2#following--retrieve-blogs-following) |
| [List Blog Likes](actions/list-blog-likes.md) | `GET /v2/blog/:blogIdentifier/likes` | [docs](https://www.tumblr.com/docs/en/api/v2#likes--retrieve-blogs-likes) |
| [List Blog Notifications](actions/list-blog-notifications.md) | `GET /v2/blog/:blogIdentifier/notifications` | [docs](https://www.tumblr.com/docs/en/api/v2#notifications--retrieve-blogs-activity-feed) |
| [List Draft Posts](actions/list-draft-posts.md) | `GET /v2/blog/:blogIdentifier/posts/draft` | [docs](https://www.tumblr.com/docs/en/api/v2#postsdraft--retrieve-draft-posts) |
| [List Queued Posts](actions/list-queued-posts.md) | `GET /v2/blog/:blogIdentifier/posts/queue` | [docs](https://www.tumblr.com/docs/en/api/v2#postsqueue--retrieve-queued-posts) |
| [List Submission Posts](actions/list-submission-posts.md) | `GET /v2/blog/:blogIdentifier/posts/submission` | [docs](https://www.tumblr.com/docs/en/api/v2#postssubmission--retrieve-submission-posts) |
| [List Tagged Posts](actions/list-tagged-posts.md) | `GET /v2/tagged` | [docs](https://www.tumblr.com/docs/en/api/v2#tagged--get-posts-with-tag) |
| [List User Following](actions/list-user-following.md) | `GET /v2/user/following` | [docs](https://www.tumblr.com/docs/en/api/v2#userfollowing--retrieve-the-blogs-a-user-is-following) |
| [List User Likes](actions/list-user-likes.md) | `GET /v2/user/likes` | [docs](https://www.tumblr.com/docs/en/api/v2#userlikes--retrieve-a-users-likes) |
| [Reblog Post (NPF)](actions/reblog-post-npf.md) | `POST /v2/blog/:blogIdentifier/posts` | [docs](https://www.tumblr.com/docs/en/api/v2#posts---createreblog-a-post-neue-post-format) |
| [Reorder Queued Posts](actions/reorder-queued-posts.md) | `POST /v2/blog/:blogIdentifier/posts/queue/reorder` | [docs](https://www.tumblr.com/docs/en/api/v2#postsqueuereorder--reorder-queued-posts) |
| [Shuffle Queued Posts](actions/shuffle-queued-posts.md) | `POST /v2/blog/:blogIdentifier/posts/queue/shuffle` | [docs](https://www.tumblr.com/docs/en/api/v2#postsqueueshuffle---shuffle-queued-posts) |
| [Unfollow Blog](actions/unfollow-blog.md) | `POST /v2/user/unfollow` | [docs](https://www.tumblr.com/docs/en/api/v2#userunfollow--unfollow-a-blog) |
| [Unlike Post](actions/unlike-post.md) | `POST /v2/user/unlike` | [docs](https://www.tumblr.com/docs/en/api/v2#userunlike--unlike-a-post) |
| [Update Post (NPF)](actions/update-post-npf.md) | `PUT /v2/blog/:blogIdentifier/posts/:postId` | [docs](https://www.tumblr.com/docs/en/api/v2#postspost-id---editing-a-post-neue-post-format) |
