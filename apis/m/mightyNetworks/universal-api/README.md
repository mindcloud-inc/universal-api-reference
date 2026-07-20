# <img src="https://images.mindcloud.co/apps/icons/mighty-networks_1773085714746.png" alt="Mighty Networks logo" width="28" height="28"> Mighty Networks: Universal API

Manage Mighty Networks members, spaces, posts, comments, plans, and events

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mightyNetworks/latest
- **Category:** Marketing / Social Media
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mightynetworks.com
- **Vendor API docs:** https://docs.mightynetworks.com/admin-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-current-user?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Post Comment](actions/create-post-comment.md) | POST | Creates a comment on a post in Mighty Networks. |
| [Delete Post Comment](actions/delete-post-comment.md) | DELETE | Deletes a comment from a post in Mighty Networks. |
| [List Post Comments](actions/list-post-comments.md) | GET | Retrieves comments for a Mighty Networks post. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Comment](actions/get-post-comment.md) | GET | Retrieves a comment from a Mighty Networks post. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Mighty Networks. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a Mighty Networks network. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Mighty Networks. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Mighty Networks. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Delete Space](actions/delete-space.md) | DELETE | Deletes an existing space from Mighty Networks. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Space Member](actions/add-space-member.md) | POST | Adds a member to a space in Mighty Networks. |
| [Get Network Member](actions/get-network-member.md) | GET | Retrieves a network member from Mighty Networks. |
| [Get Network Member by Email](actions/get-network-member-by-email.md) | GET | Finds a network member in Mighty Networks by email address. |
| [List Network Members](actions/list-network-members.md) | GET | Retrieves members from the current Mighty Networks network. |
| [List Space Members](actions/list-space-members.md) | GET | Retrieves members from a space in Mighty Networks. |
| [Remove Space Member](actions/remove-space-member.md) | DELETE | Removes a member from a space in Mighty Networks. |
| [Update Network Member](actions/update-network-member.md) | PUT | Updates a member's role in Mighty Networks. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post or article from Mighty Networks. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET | Retrieves a plan from Mighty Networks. |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from a Mighty Networks network. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Mighty Networks with optional notifications. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post from Mighty Networks. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from a Mighty Networks network. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post or article in Mighty Networks. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST | Creates a new space in Mighty Networks. |
| [Get Space](actions/get-space.md) | GET | Retrieves a space from Mighty Networks. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from a Mighty Networks network. |
| [Update Space](actions/update-space.md) | PUT | Updates an existing space in Mighty Networks. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Archive Plan](actions/archive-plan.md) | DELETE | Archives a plan in Mighty Networks, canceling subscriptions and revoking access. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Mighty Networks. |

