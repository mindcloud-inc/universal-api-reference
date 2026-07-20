# <img src="https://images.mindcloud.co/apps/icons/beamer_1773678914443.png" alt="Beamer logo" width="28" height="28"> Beamer: Universal API

Manage product announcements, posts, unread counts, and NPS checks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/beamer/latest
- **Category:** Support / Customer Success
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getbeamer.com/
- **Vendor API docs:** https://help.userflow.com/beamer/docs/beamer-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Post Comments](actions/count-post-comments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/count-post-comments?connectionId=$CONNECTION_ID&postId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Announcement

| Action | Method | Description |
| --- | --- | --- |
| [Count Posts](actions/count-posts.md) | GET | Retrieves a post count from Beamer. |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Beamer. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from Beamer. |
| [Get Post By ID](actions/get-post-by-id.md) | GET | Retrieves a post from Beamer by ID. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Beamer. |
| [List Unread Posts](actions/list-unread-posts.md) | GET | Retrieves unread posts from Beamer. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in Beamer. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Post Comment](actions/create-post-comment.md) | POST | Creates a new post comment in Beamer. |
| [List Post Comments](actions/list-post-comments.md) | GET | Retrieves comments for a post from Beamer. |

### Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed URL](actions/get-feed-url.md) | GET | Retrieves the Beamer feed URL for a user. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Post Reaction](actions/create-post-reaction.md) | GET | Creates a post reaction in Beamer. |
| [Delete Post Reaction](actions/delete-post-reaction.md) | DELETE | Deletes a post reaction from Beamer. |
| [Ping API](actions/ping-api.md) | POST | Pings the Beamer API to verify connectivity. |

### Post Comments

| Action | Method | Description |
| --- | --- | --- |
| [Count Post Comments](actions/count-post-comments.md) | GET | Retrieves a post comment count from Beamer. |

### Post Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Count Post Reactions](actions/count-post-reactions.md) | GET | Retrieves a post reaction count from Beamer. |
| [Get Post Reaction By ID](actions/get-post-reaction-by-id.md) | GET | Retrieves a post reaction from Beamer. |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [List Post Reactions](actions/list-post-reactions.md) | GET | Retrieves reactions for a post from Beamer. |

### Unread Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Unread Count](actions/get-unread-count.md) | GET | Retrieves the unread post count from Beamer. |

