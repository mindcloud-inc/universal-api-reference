# <img src="https://images.mindcloud.co/apps/icons/circle_1773159258284.png" alt="Circle logo" width="28" height="28"> Circle: Universal API

Manage Circle communities, members, spaces, posts, events, and access groups

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/circle/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://circle.so
- **Vendor API docs:** https://api.circle.so/apis/admin-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Basic Post](actions/get-basic-post.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-basic-post?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Create Basic Post](actions/create-basic-post.md) | POST | Creates a new basic post in Circle. |
| [Get Basic Post](actions/get-basic-post.md) | GET | Retrieves basic post details from Circle by ID. |
| [List Basic Posts](actions/list-basic-posts.md) | GET | Retrieves basic post records from Circle. |
| [Update Basic Post](actions/update-basic-post.md) | PUT | Updates an existing basic post in Circle. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST | Creates a new space in Circle. |
| [Get Space](actions/get-space.md) | GET | Retrieves space details from Circle by ID. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves space records from your Circle community. |
| [Update Space](actions/update-space.md) | PUT | Updates an existing space in Circle. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Circle. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves comment details from Circle by ID. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comment records from your Circle community. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Profile Fields](actions/list-profile-fields.md) | GET | Retrieves profile field records from Circle. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Circle. |
| [Get Event](actions/get-event.md) | GET | Retrieves event details from Circle by ID. |
| [List Events](actions/list-events.md) | GET | Retrieves event records from your Circle community. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Circle. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Access Group](actions/create-access-group.md) | POST | Creates a new access group in Circle. |
| [List Access Groups](actions/list-access-groups.md) | GET | Retrieves access group records from Circle. |
| [Update Access Group](actions/update-access-group.md) | PUT | Updates an existing access group in Circle. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Add Space Member](actions/add-space-member.md) | POST | Creates a new space membership in Circle. |
| [List Community Member Spaces](actions/list-community-member-spaces.md) | GET | Retrieves community member space memberships from Circle. |
| [List Space Members](actions/list-space-members.md) | GET | Retrieves space membership records from Circle. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Create Community Segment](actions/create-community-segment.md) | POST | Creates a new community segment in Circle. |
| [List Community Segments](actions/list-community-segments.md) | GET | Retrieves community segment records from Circle. |
| [Update Community Segment](actions/update-community-segment.md) | PUT | Updates an existing community segment in Circle. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Member Tag](actions/create-member-tag.md) | POST | Creates a new member tag in Circle. |
| [Get Member Tag](actions/get-member-tag.md) | GET | Retrieves member tag details from Circle by ID. |
| [List Member Tags](actions/list-member-tags.md) | GET | Retrieves member tag records from Circle. |
| [Update Member Tag](actions/update-member-tag.md) | PUT | Updates an existing member tag in Circle. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Community](actions/get-community.md) | GET | Retrieves current community details from Circle. |
| [Update Community](actions/update-community.md) | PUT | Updates current community details in Circle. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Create Topic](actions/create-topic.md) | POST | Creates a new topic in Circle. |
| [Get Topic](actions/get-topic.md) | GET | Retrieves topic details from Circle by ID. |
| [List Topics](actions/list-topics.md) | GET | Retrieves topic records from your Circle community. |
| [Update Topic](actions/update-topic.md) | PUT | Updates an existing topic in Circle. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Community Member](actions/create-community-member.md) | POST | Creates a new community member in Circle. |
| [Get Community Member](actions/get-community-member.md) | GET | Retrieves community member details from Circle by ID. |
| [List Community Members](actions/list-community-members.md) | GET | Retrieves community member records from Circle. |
| [Search Community Members](actions/search-community-members.md) | GET | Finds community members in Circle by search query. |
| [Update Community Member](actions/update-community-member.md) | PUT | Updates an existing community member in Circle. |

