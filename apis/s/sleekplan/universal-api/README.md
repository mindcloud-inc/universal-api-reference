# <img src="https://images.mindcloud.co/apps/icons/sleekplan_1775657135118.png" alt="Sleekplan logo" width="28" height="28"> Sleekplan: Universal API

Collect feedback, manage roadmaps, publish changelogs, and track satisfaction

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sleekplan/latest
- **Category:** Support / Customer Success
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sleekplan.com/
- **Vendor API docs:** https://sleekplan.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Updates](actions/list-updates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-updates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [Delete Comment](actions/delete-comment.md) | DELETE |  |
| [Get Comment](actions/get-comment.md) | GET |  |
| [Like Comment](actions/like-comment.md) | POST |  |
| [List Comments](actions/list-comments.md) | GET |  |
| [Update Comment](actions/update-comment.md) | PUT |  |

### Intelligence Queue

| Action | Method | Description |
| --- | --- | --- |
| [Send Content to Intelligence Queue](actions/send-content-to-intelligence-queue.md) | POST |  |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Unread Notification Count](actions/get-unread-notification-count.md) | GET |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST |  |
| [Delete Post](actions/delete-post.md) | DELETE |  |
| [Get Post](actions/get-post.md) | GET |  |
| [List Posts](actions/list-posts.md) | GET |  |
| [Update Post](actions/update-post.md) | PUT |  |

### Post Meta

| Action | Method | Description |
| --- | --- | --- |
| [Delete Post Metadata](actions/delete-post-metadata.md) | DELETE |  |
| [Get Post Metadata](actions/get-post-metadata.md) | GET |  |
| [Update Post Metadata](actions/update-post-metadata.md) | PUT |  |

### Promoter Response

| Action | Method | Description |
| --- | --- | --- |
| [Create NPS Response](actions/create-nps-response.md) | POST |  |
| [List NPS Responses](actions/list-nps-responses.md) | GET |  |

### Satisfaction Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Satisfaction Response](actions/create-satisfaction-response.md) | POST |  |
| [Create Update Satisfaction Response](actions/create-update-satisfaction-response.md) | POST |  |
| [List Satisfaction Responses](actions/list-satisfaction-responses.md) | GET |  |
| [List Update Satisfaction Responses](actions/list-update-satisfaction-responses.md) | GET |  |

### Update

| Action | Method | Description |
| --- | --- | --- |
| [Create Update](actions/create-update.md) | POST |  |
| [Delete Update](actions/delete-update.md) | DELETE |  |
| [Edit Update](actions/edit-update.md) | PUT |  |
| [Get Update](actions/get-update.md) | GET |  |
| [List Updates](actions/list-updates.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

### Vote

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Vote](actions/create-or-update-vote.md) | PUT |  |
| [List Votes](actions/list-votes.md) | GET |  |

