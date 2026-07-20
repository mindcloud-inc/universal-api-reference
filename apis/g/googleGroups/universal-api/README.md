# <img src="https://images.mindcloud.co/apps/icons/google-groups_1774468383627.png" alt="Google Groups logo" width="28" height="28"> Google Groups: Universal API

Manage Google Groups, memberships, aliases, and group settings in Google Workspace.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleGroups/latest
- **Category:** Communication / Team Messaging
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://groups.google.com
- **Vendor API docs:** https://developers.google.com/workspace/admin/directory/v1/guides/manage-groups

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Alias

| Action | Method | Description |
| --- | --- | --- |
| [Delete Group Alias](actions/delete-group-alias.md) | DELETE | Deletes a group alias from Google Groups. |
| [List Group Aliases](actions/list-group-aliases.md) | GET | Retrieves aliases for a group from Google Groups. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Google Groups. |
| [Create Group Alias](actions/create-group-alias.md) | POST | Creates a group alias in Google Groups. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Google Groups. |
| [Get Group](actions/get-group.md) | GET | Retrieves a Google Group by key. |
| [Get Group Settings](actions/get-group-settings.md) | GET | Retrieves settings for a group in Google Groups. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Google Groups for a domain or user. |
| [Patch Group](actions/patch-group.md) | PUT | Updates an existing group in Google Groups. |
| [Update Group](actions/update-group.md) | PUT | Replaces an existing group in Google Groups. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Member](actions/add-group-member.md) | POST | Adds a member to a group in Google Groups. |
| [Delete Group Member](actions/delete-group-member.md) | DELETE | Deletes an existing group member from Google Groups. |
| [Get Group Member](actions/get-group-member.md) | GET | Retrieves a group member from Google Groups. |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves members of a group from Google Groups. |
| [Patch Group Member](actions/patch-group-member.md) | PUT | Updates an existing group member in Google Groups. |
| [Update Group Member](actions/update-group-member.md) | PUT | Replaces an existing group member in Google Groups. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Check Group Membership](actions/check-group-membership.md) | GET | Checks whether a member belongs to a group in Google Groups. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [Update Group Settings](actions/update-group-settings.md) | PUT | Replaces group settings in Google Groups. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Patch Group Settings](actions/patch-group-settings.md) | PUT | Updates group settings in Google Groups. |

