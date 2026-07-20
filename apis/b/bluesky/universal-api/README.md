# <img src="https://images.mindcloud.co/apps/icons/bluesky_1775589522313.png" alt="Bluesky logo" width="28" height="28"> Bluesky: Universal API

Read Bluesky profiles, feeds, notifications, social graph data, and account session details through the official atproto HTTP API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bluesky/latest
- **Category:** Marketing / Social Media
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bsky.app
- **Vendor API docs:** https://docs.bsky.app/docs/category/http-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Session](actions/get-session.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Actor Feeds](actions/get-actor-feeds.md) | GET | Retrieves Bluesky feeds created by a specific actor. |
| [Get Author Feed](actions/get-author-feed.md) | GET | Retrieves posts and reposts from a Bluesky actor. |
| [Get Feed](actions/get-feed.md) | GET | Retrieves posts from a selected Bluesky feed. |
| [Get Feed Generator](actions/get-feed-generator.md) | GET | Retrieves details for a Bluesky feed generator. |
| [Get Likes](actions/get-likes.md) | GET | Retrieves likes for a Bluesky post by URI. |
| [Get Quotes](actions/get-quotes.md) | GET | Retrieves quote posts for a specific Bluesky post. |
| [Get Suggested Feeds](actions/get-suggested-feeds.md) | GET | Retrieves suggested Bluesky feeds for the current account. |
| [Get Timeline](actions/get-timeline.md) | GET | Retrieves the current account's Bluesky home timeline. |
| [Search Posts](actions/search-posts.md) | GET | Finds Bluesky posts matching a search query. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [List App Passwords](actions/list-app-passwords.md) | GET | Retrieves app passwords for the current Bluesky account. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Actor Starter Packs](actions/get-actor-starter-packs.md) | GET | Retrieves Bluesky starter packs created by a specific actor. |
| [Get List](actions/get-list.md) | GET | Retrieves details for a specific Bluesky list. |
| [Get List Feed](actions/get-list-feed.md) | GET | Retrieves recent posts from a Bluesky list. |
| [Get Lists](actions/get-lists.md) | GET | Retrieves Bluesky lists created by a specific account. |
| [Get Lists With Membership](actions/get-lists-with-membership.md) | GET | Retrieves the current account's Bluesky lists with membership for a specific actor. |
| [Get Starter Pack](actions/get-starter-pack.md) | GET | Retrieves details for a specific Bluesky starter pack. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Get Unread Count](actions/get-unread-count.md) | GET | Retrieves the current Bluesky unread notification count. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications for the current Bluesky account. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Describe Server](actions/describe-server.md) | GET | Retrieves Bluesky server capabilities and account creation requirements. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET | Retrieves the current Bluesky session details. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Subscriptions](actions/list-activity-subscriptions.md) | GET | Retrieves accounts the current Bluesky account subscribes to for notifications. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Thread](actions/get-post-thread.md) | GET | Retrieves a thread for a specific Bluesky post. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Followers](actions/get-followers.md) | GET | Retrieves followers for a specific Bluesky account. |
| [Get Follows](actions/get-follows.md) | GET | Retrieves accounts followed by a specific Bluesky account. |
| [Get Mutes](actions/get-mutes.md) | GET | Retrieves muted Bluesky accounts for the current account. |
| [Get Preferences](actions/get-preferences.md) | GET | Retrieves the current account's private Bluesky preferences. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a Bluesky profile by handle or DID. |
| [Get Reposted By](actions/get-reposted-by.md) | GET | Retrieves accounts that reposted a specific Bluesky post. |
| [Get Suggested Follows By Actor](actions/get-suggested-follows-by-actor.md) | GET | Retrieves Bluesky follow suggestions similar to a specific actor. |
| [Get Suggestions](actions/get-suggestions.md) | GET | Retrieves suggested Bluesky accounts to follow. |
| [Search Actors](actions/search-actors.md) | GET | Finds Bluesky profiles matching a search query. |
| [Search Actors Typeahead](actions/search-actors-typeahead.md) | GET | Finds Bluesky profile suggestions by search prefix. |

