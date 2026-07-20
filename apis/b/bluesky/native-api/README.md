# Bluesky: Native API Reference

A consolidated summary of Bluesky's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.bsky.app/docs/category/http-reference
- **API base URL:** `{pdsUrl}`

## Authentication

### Session Token

Use a Bluesky app-password session and the resolved PDS URL for authenticated Bluesky and atproto requests.

### Credentials

- **Access Token:** `accessToken` · required · Paste the accessJwt returned by com.atproto.server.createSession.
- **Refresh Token:** `refreshToken` · required · Paste the refreshJwt returned by com.atproto.server.createSession.
- **PDS URL:** `pdsUrl` · required · Paste didDoc.service[0].serviceEndpoint from the createSession response, including https://.
- **DID:** `did` · required · Paste the did value returned by com.atproto.server.createSession.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://docs.bsky.app/docs/advanced-guides/api-directory)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Describe Server](actions/describe-server.md) | `GET /xrpc/com.atproto.server.describeServer` | [docs](https://docs.bsky.app/docs/api/com-atproto-server-describe-server) |
| [Get Actor Feeds](actions/get-actor-feeds.md) | `GET /xrpc/app.bsky.feed.getActorFeeds` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-actor-feeds) |
| [Get Actor Starter Packs](actions/get-actor-starter-packs.md) | `GET /xrpc/app.bsky.graph.getActorStarterPacks` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-actor-starter-packs) |
| [Get Author Feed](actions/get-author-feed.md) | `GET /xrpc/app.bsky.feed.getAuthorFeed` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-author-feed) |
| [Get Feed](actions/get-feed.md) | `GET /xrpc/app.bsky.feed.getFeed` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-feed) |
| [Get Feed Generator](actions/get-feed-generator.md) | `GET /xrpc/app.bsky.feed.getFeedGenerator` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-feed-generator) |
| [Get Followers](actions/get-followers.md) | `GET /xrpc/app.bsky.graph.getFollowers` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-followers) |
| [Get Follows](actions/get-follows.md) | `GET /xrpc/app.bsky.graph.getFollows` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-follows) |
| [Get Likes](actions/get-likes.md) | `GET /xrpc/app.bsky.feed.getLikes` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-likes) |
| [Get List](actions/get-list.md) | `GET /xrpc/app.bsky.graph.getList` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-list) |
| [Get List Feed](actions/get-list-feed.md) | `GET /xrpc/app.bsky.feed.getListFeed` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-list-feed) |
| [Get Lists](actions/get-lists.md) | `GET /xrpc/app.bsky.graph.getLists` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-lists) |
| [Get Lists With Membership](actions/get-lists-with-membership.md) | `GET /xrpc/app.bsky.graph.getListsWithMembership` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-lists-with-membership) |
| [Get Mutes](actions/get-mutes.md) | `GET /xrpc/app.bsky.graph.getMutes` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-mutes) |
| [Get Post Thread](actions/get-post-thread.md) | `GET /xrpc/app.bsky.feed.getPostThread` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-post-thread) |
| [Get Preferences](actions/get-preferences.md) | `GET /xrpc/app.bsky.actor.getPreferences` | [docs](https://docs.bsky.app/docs/api/app-bsky-actor-get-preferences) |
| [Get Profile](actions/get-profile.md) | `GET /xrpc/app.bsky.actor.getProfile` | [docs](https://docs.bsky.app/docs/api/app-bsky-actor-get-profile) |
| [Get Quotes](actions/get-quotes.md) | `GET /xrpc/app.bsky.feed.getQuotes` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-quotes) |
| [Get Reposted By](actions/get-reposted-by.md) | `GET /xrpc/app.bsky.feed.getRepostedBy` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-reposted-by) |
| [Get Session](actions/get-session.md) | `GET /xrpc/com.atproto.server.getSession` | [docs](https://docs.bsky.app/docs/api/com-atproto-server-get-session) |
| [Get Starter Pack](actions/get-starter-pack.md) | `GET /xrpc/app.bsky.graph.getStarterPack` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-starter-pack) |
| [Get Suggested Feeds](actions/get-suggested-feeds.md) | `GET /xrpc/app.bsky.feed.getSuggestedFeeds` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-suggested-feeds) |
| [Get Suggested Follows By Actor](actions/get-suggested-follows-by-actor.md) | `GET /xrpc/app.bsky.graph.getSuggestedFollowsByActor` | [docs](https://docs.bsky.app/docs/api/app-bsky-graph-get-suggested-follows-by-actor) |
| [Get Suggestions](actions/get-suggestions.md) | `GET /xrpc/app.bsky.actor.getSuggestions` | [docs](https://docs.bsky.app/docs/api/app-bsky-actor-get-suggestions) |
| [Get Timeline](actions/get-timeline.md) | `GET /xrpc/app.bsky.feed.getTimeline` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-get-timeline) |
| [Get Unread Count](actions/get-unread-count.md) | `GET /xrpc/app.bsky.notification.getUnreadCount` | [docs](https://docs.bsky.app/docs/api/app-bsky-notification-get-unread-count) |
| [List Activity Subscriptions](actions/list-activity-subscriptions.md) | `GET /xrpc/app.bsky.notification.listActivitySubscriptions` | [docs](https://docs.bsky.app/docs/api/app-bsky-notification-list-activity-subscriptions) |
| [List App Passwords](actions/list-app-passwords.md) | `GET /xrpc/com.atproto.server.listAppPasswords` | [docs](https://docs.bsky.app/docs/api/com-atproto-server-list-app-passwords) |
| [List Notifications](actions/list-notifications.md) | `GET /xrpc/app.bsky.notification.listNotifications` | [docs](https://docs.bsky.app/docs/api/app-bsky-notification-list-notifications) |
| [Search Actors](actions/search-actors.md) | `GET /xrpc/app.bsky.actor.searchActors` | [docs](https://docs.bsky.app/docs/api/app-bsky-actor-search-actors) |
| [Search Actors Typeahead](actions/search-actors-typeahead.md) | `GET /xrpc/app.bsky.actor.searchActorsTypeahead` | [docs](https://docs.bsky.app/docs/api/app-bsky-actor-search-actors-typeahead) |
| [Search Posts](actions/search-posts.md) | `GET /xrpc/app.bsky.feed.searchPosts` | [docs](https://docs.bsky.app/docs/api/app-bsky-feed-search-posts) |
