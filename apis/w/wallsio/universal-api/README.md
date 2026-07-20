# <img src="https://images.mindcloud.co/apps/icons/wallsio_1774877375202.png" alt="Walls.io logo" width="28" height="28"> Walls.io: Universal API

Manage Walls.io wall content and moderation via the Walls.io API, including posts, analytics, ads, and user moderation controls.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wallsio/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://walls.io
- **Vendor API docs:** https://github.com/DieSocialisten/Walls.io-API-Docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Posts](actions/list-posts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/list-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Ad

| Action | Method | Description |
| --- | --- | --- |
| [List Ads](actions/list-ads.md) | GET | Retrieves sponsored posts from Walls.io. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Clear Post Spam](actions/clear-post-spam.md) | PUT | Clears a post spam status in Walls.io. |
| [Create Hidden Post](actions/create-hidden-post.md) | POST | Creates a new hidden post in Walls.io. |
| [Create Image Post](actions/create-image-post.md) | POST | Creates a new image post in Walls.io. |
| [Create Pinned Post](actions/create-pinned-post.md) | POST | Creates a new pinned post in Walls.io. |
| [Create Scheduled Post](actions/create-scheduled-post.md) | POST | Creates a new scheduled post in Walls.io. |
| [Create Text Post](actions/create-text-post.md) | POST | Creates a new text post in Walls.io. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post from Walls.io by post ID. |
| [Get Post Analytics](actions/get-post-analytics.md) | GET | Retrieves post counts by network from Walls.io. |
| [Get Post Analytics By Type](actions/get-post-analytics-by-type.md) | GET | Retrieves post counts for selected post types from Walls.io. |
| [Get Post With Source](actions/get-post-with-source.md) | GET | Retrieves a post with source details from Walls.io. |
| [List Changed Pinned Posts](actions/list-changed-pinned-posts.md) | GET | Retrieves pinned posts updated since a timestamp from Walls.io. |
| [List Changed Posts](actions/list-changed-posts.md) | GET | Retrieves posts updated since a timestamp from Walls.io. |
| [List Changed Posts By Language](actions/list-changed-posts-by-language.md) | GET | Finds updated posts in Walls.io by language. |
| [List Changed Posts By Media Type](actions/list-changed-posts-by-media-type.md) | GET | Finds updated posts in Walls.io by media type. |
| [List Changed Posts By Type](actions/list-changed-posts-by-type.md) | GET | Finds updated posts in Walls.io by post type. |
| [List Pinned Posts](actions/list-pinned-posts.md) | GET | Retrieves pinned posts from Walls.io. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Walls.io. |
| [List Posts After ID](actions/list-posts-after-id.md) | GET | Finds posts in Walls.io after a post ID. |
| [List Posts Before ID](actions/list-posts-before-id.md) | GET | Finds posts in Walls.io before a post ID. |
| [List Posts By Language](actions/list-posts-by-language.md) | GET | Finds posts in Walls.io by language. |
| [List Posts By Media Type](actions/list-posts-by-media-type.md) | GET | Finds posts in Walls.io by media type. |
| [List Posts By Type](actions/list-posts-by-type.md) | GET | Finds posts in Walls.io by post type. |
| [List Posts With Source](actions/list-posts-with-source.md) | GET | Retrieves posts with source details from Walls.io. |
| [Pin Post](actions/pin-post.md) | PUT | Pins a post in Walls.io. |
| [Report Post Spam](actions/report-post-spam.md) | PUT | Reports a post as spam in Walls.io. |
| [Unpin Post](actions/unpin-post.md) | PUT | Unpins a post in Walls.io. |
| [Update Post Language](actions/update-post-language.md) | PUT | Updates a post language in Walls.io. |
| [Update Post Visibility](actions/update-post-visibility.md) | PUT | Updates a post visibility status in Walls.io. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Analytics](actions/get-user-analytics.md) | GET | Retrieves unique user counts by network from Walls.io. |
| [Get User Analytics By Type](actions/get-user-analytics-by-type.md) | GET | Retrieves unique user counts for selected post types from Walls.io. |

