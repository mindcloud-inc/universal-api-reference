# <img src="https://images.mindcloud.co/apps/icons/tumblr_1772824096009.png" alt="Tumblr logo" width="28" height="28"> Tumblr: Universal API

Create posts, follow blogs, and manage blog engagement

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tumblr/latest
- **Category:** Marketing / Social Media
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tumblr.com
- **Vendor API docs:** https://www.tumblr.com/docs/en/api/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check If Blog Is Followed By Another Blog](actions/check-if-blog-is-followed-by-another-blog.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/check-if-blog-is-followed-by-another-blog?connectionId=$CONNECTION_ID&blogIdentifier=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Blog

| Action | Method | Description |
| --- | --- | --- |
| [Check If Blog Is Followed By Another Blog](actions/check-if-blog-is-followed-by-another-blog.md) | GET | Checks whether a Tumblr blog is followed by another blog. |
| [Follow Blog](actions/follow-blog.md) | POST | Follows a Tumblr blog from the user account. |
| [Get Blog Avatar](actions/get-blog-avatar.md) | GET | Retrieves a Tumblr blog avatar by size. |
| [Get Blog Info](actions/get-blog-info.md) | GET | Retrieves information for a Tumblr blog. |
| [List Blog Blocks](actions/list-blog-blocks.md) | GET | Retrieves blocked blogs for a Tumblr blog. |
| [List Blog Following](actions/list-blog-following.md) | GET | Retrieves blogs followed by a Tumblr blog. |
| [List User Following](actions/list-user-following.md) | GET | Retrieves blogs followed by the Tumblr user. |
| [Unfollow Blog](actions/unfollow-blog.md) | DELETE | Unfollows a Tumblr blog from the user account. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Notes](actions/get-post-notes.md) | GET | Retrieves notes for a Tumblr post. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Blog Notifications](actions/list-blog-notifications.md) | GET | Retrieves activity notifications for a Tumblr blog. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post (NPF)](actions/create-post-npf.md) | POST | Creates a new Tumblr post using NPF. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from Tumblr. |
| [Get Post (NPF)](actions/get-post-npf.md) | GET | Retrieves a Tumblr post using NPF. |
| [Get Published Blog Posts](actions/get-published-blog-posts.md) | GET | Retrieves published posts from a Tumblr blog. |
| [Get User Dashboard](actions/get-user-dashboard.md) | GET | Retrieves the authenticated user's Tumblr dashboard. |
| [Like Post](actions/like-post.md) | POST | Likes a Tumblr post from the user account. |
| [List Blog Likes](actions/list-blog-likes.md) | GET | Retrieves liked posts from a Tumblr blog. |
| [List Draft Posts](actions/list-draft-posts.md) | GET | Retrieves draft posts from a Tumblr blog. |
| [List Queued Posts](actions/list-queued-posts.md) | GET | Retrieves queued posts from a Tumblr blog. |
| [List Submission Posts](actions/list-submission-posts.md) | GET | Retrieves submission posts from a Tumblr blog. |
| [List Tagged Posts](actions/list-tagged-posts.md) | GET | Retrieves Tumblr posts with a specific tag. |
| [List User Likes](actions/list-user-likes.md) | GET | Retrieves posts liked by the Tumblr user. |
| [Reblog Post (NPF)](actions/reblog-post-npf.md) | POST | Reblogs a Tumblr post using NPF. |
| [Unlike Post](actions/unlike-post.md) | DELETE | Removes a like from a Tumblr post. |
| [Update Post (NPF)](actions/update-post-npf.md) | PUT | Updates an existing Tumblr post using NPF. |

### Post Queue

| Action | Method | Description |
| --- | --- | --- |
| [Reorder Queued Posts](actions/reorder-queued-posts.md) | PUT | Reorders queued posts in a Tumblr blog. |
| [Shuffle Queued Posts](actions/shuffle-queued-posts.md) | PUT | Shuffles queued posts in a Tumblr blog. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves account information for the Tumblr user. |
| [Get User Limits](actions/get-user-limits.md) | GET | Retrieves Tumblr posting limits for the user. |
| [List Blog Followers](actions/list-blog-followers.md) | GET | Retrieves followers of a Tumblr blog. |

