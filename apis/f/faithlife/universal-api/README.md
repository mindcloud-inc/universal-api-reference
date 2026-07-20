# <img src="https://images.mindcloud.co/apps/icons/faithlife_1775682627765.png" alt="Faithlife logo" width="28" height="28"> Faithlife: Universal API

Build communities, groups, and church engagement experiences on the Faithlife platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/faithlife/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://faithlife.com/
- **Vendor API docs:** https://developer.faithlife.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Newsfeed](actions/get-group-newsfeed.md) | GET | Retrieves a group's newsfeed from Faithlife. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Faithlife. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Faithlife. |
| [List Groups For User](actions/list-groups-for-user.md) | GET | Retrieves a user's groups from Faithlife. |
| [Search Groups](actions/search-groups.md) | GET | Finds groups in Faithlife. |

### Invite

| Action | Method | Description |
| --- | --- | --- |
| [Invite Users To Group](actions/invite-users-to-group.md) | POST | Creates invites for a group in Faithlife. |
| [List Group Invites](actions/list-group-invites.md) | GET | Retrieves a group's invites from Faithlife. |
| [List My Invites](actions/list-my-invites.md) | GET | Retrieves the current user's invites from Faithlife. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Accept Invite To Group](actions/accept-invite-to-group.md) | POST | Accepts a group invite in Faithlife. |
| [Delete Membership](actions/delete-membership.md) | DELETE | Deletes a group membership from Faithlife. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Faithlife. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Faithlife. |
| [Search Users](actions/search-users.md) | GET | Finds users in Faithlife. |

