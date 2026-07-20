# <img src="https://images.mindcloud.co/apps/icons/xenforo_1776713246396.png" alt="XenForo logo" width="28" height="28"> XenForo: Universal API

XenForo community forum API integration for reading and managing forums, threads, posts, users, alerts, and site metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xenForo/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xenforo.com
- **Vendor API docs:** https://docs.xenforo.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site Info](actions/get-site-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-site-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert](actions/get-alert.md) | GET | Retrieves the specified alert from XenForo. |
| [Get Alerts](actions/get-alerts.md) | GET | Retrieves a list of user alerts from XenForo. |
| [Mark Alert](actions/mark-alert.md) | PUT | Updates an alert's read or viewed status in XenForo. |
| [Send Alert](actions/send-alert.md) | POST | Sends an alert to a user in XenForo. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Forum](actions/get-forum.md) | GET | Retrieves the specified forum from XenForo. |
| [Mark Forum Read](actions/mark-forum-read.md) | PUT | Marks a forum as read in XenForo. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Thread Reply](actions/add-thread-reply.md) | POST | Creates a reply post in XenForo. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from XenForo. |
| [Get Post](actions/get-post.md) | GET | Retrieves the specified post from XenForo. |
| [Get Thread Posts](actions/get-thread-posts.md) | GET | Retrieves posts from a thread in XenForo. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in XenForo. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Flattened Node Tree](actions/get-flattened-node-tree.md) | GET | Retrieves the flattened node tree from XenForo. |
| [Get Node](actions/get-node.md) | GET | Retrieves the specified node from XenForo. |
| [Get Node Tree](actions/get-node-tree.md) | GET | Retrieves the node tree from XenForo. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [React To Post](actions/react-to-post.md) | POST | Creates a reaction on a post in XenForo. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Statistics](actions/get-site-statistics.md) | GET | Retrieves public site statistics from XenForo. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | POST | Creates a new thread in XenForo. |
| [Get Forum Threads](actions/get-forum-threads.md) | GET | Retrieves a page of forum threads from XenForo. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves the specified thread from XenForo. |
| [Get Threads](actions/get-threads.md) | GET | Retrieves a list of threads from XenForo. |
| [Update Thread](actions/update-thread.md) | PUT | Updates an existing thread in XenForo. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from XenForo. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the specified user from XenForo. |
| [Get Users](actions/get-users.md) | GET | Retrieves a list of users from XenForo. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Info](actions/get-site-info.md) | GET | Retrieves site and API information from XenForo. |

