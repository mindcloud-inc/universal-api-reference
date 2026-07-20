# <img src="https://images.mindcloud.co/apps/icons/favicon-www-are-na-48x48_1777381254683.png" alt="Are.na logo" width="28" height="28"> Are.na: Universal API

Are.na is a platform for collecting and connecting blocks of content in channels, with API access to users, channels, blocks, comments, connections, groups, and search.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/are-na/latest
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.are.na
- **Vendor API docs:** https://www.are.na/developers/explore

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Are.na. |
| [Delete Channel](actions/delete-channel.md) | DELETE | Deletes an existing channel from Are.na. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Are.na. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Are.na. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Block Comment](actions/create-block-comment.md) | POST | Creates a new comment on a block in Are.na. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Are.na. |
| [List Block Comments](actions/list-block-comments.md) | GET | Retrieves comments for a block in Are.na. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | POST | Creates a new connection in Are.na. |
| [Delete Connection](actions/delete-connection.md) | DELETE | Deletes an existing connection from Are.na. |
| [Get Connection](actions/get-connection.md) | GET | Retrieves a connection by ID from Are.na. |
| [List Block Connections](actions/list-block-connections.md) | GET | Retrieves connections for a block in Are.na. |
| [List Channel Connections](actions/list-channel-connections.md) | GET | Retrieves connections for a channel in Are.na. |
| [Move Connection](actions/move-connection.md) | PUT | Moves a connection within a channel in Are.na. |
| [Update Connection](actions/update-connection.md) | PUT | Updates an existing connection in Are.na. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload Presign URL](actions/create-upload-presign-url.md) | POST | Creates a presigned upload URL in Are.na. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group profile from Are.na. |
| [List User Groups](actions/list-user-groups.md) | GET | Retrieves groups for a user in Are.na. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Block](actions/create-block.md) | POST | Creates a new block in Are.na. |
| [Get Block](actions/get-block.md) | GET | Retrieves a block by ID from Are.na. |
| [Get OpenAPI Specification](actions/get-open-api-specification.md) | GET | Retrieves the OpenAPI specification from Are.na. |
| [List Channel Contents](actions/list-channel-contents.md) | GET | Retrieves contents from a channel in Are.na. |
| [List Group Contents](actions/list-group-contents.md) | GET | Retrieves contents created by a group in Are.na. |
| [List User Contents](actions/list-user-contents.md) | GET | Retrieves contents created by a user in Are.na. |
| [Ping](actions/ping.md) | GET | Retrieves API health status from Are.na. |
| [Search Are.na](actions/search-arena.md) | GET | Finds blocks, channels, users, and groups in Are.na. |
| [Update Block](actions/update-block.md) | PUT | Updates an existing block in Are.na. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Are.na. |
| [Get User](actions/get-user.md) | GET | Retrieves a user profile from Are.na. |
| [List Channel Followers](actions/list-channel-followers.md) | GET | Retrieves followers for a channel in Are.na. |
| [List Group Followers](actions/list-group-followers.md) | GET | Retrieves followers for a group in Are.na. |
| [List User Followers](actions/list-user-followers.md) | GET | Retrieves followers for a user in Are.na. |
| [List User Following](actions/list-user-following.md) | GET | Retrieves who a user follows in Are.na. |

