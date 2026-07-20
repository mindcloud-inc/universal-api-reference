# <img src="https://images.mindcloud.co/apps/icons/hi-view-solutions-google-workspace-reseller_1774462610176.png" alt="Google Workspace Admin logo" width="28" height="28"> Google Workspace Admin: Universal API

Google Workspace Admin SDK scaffold for user directory automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleWorkspaceAdmin/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workspace.google.com/
- **Vendor API docs:** https://developers.google.com/workspace/admin/directory/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-users?connectionId=$CONNECTION_ID&customer=my_customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Group Members

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Member](actions/add-group-member.md) | POST | Adds a member to a Google Workspace Admin group. |
| [Check Group Membership](actions/check-group-membership.md) | GET | Checks whether a user belongs to a group in Google Workspace Admin. |
| [Get Group Member](actions/get-group-member.md) | GET | Retrieves a member from a Google Workspace Admin group. |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves members from a Google Workspace Admin group. |
| [Remove Group Member](actions/remove-group-member.md) | DELETE | Removes a member from a Google Workspace Admin group. |
| [Update Group Member](actions/update-group-member.md) | PUT | Updates a member in a Google Workspace Admin group. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Google Workspace Admin. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Google Workspace Admin. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Google Workspace Admin. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Google Workspace Admin. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Google Workspace Admin. |

### Org Units

| Action | Method | Description |
| --- | --- | --- |
| [Add Organizational Unit](actions/add-organizational-unit.md) | POST | Creates an organizational unit in Google Workspace Admin. |
| [Get Organizational Unit](actions/get-organizational-unit.md) | GET | Retrieves an organizational unit from Google Workspace Admin. |
| [List Organizational Units](actions/list-organizational-units.md) | GET | Retrieves organizational units from Google Workspace Admin. |
| [Remove Organizational Unit](actions/remove-organizational-unit.md) | DELETE | Deletes an organizational unit from Google Workspace Admin. |
| [Update Organizational Unit](actions/update-organizational-unit.md) | PUT | Updates an organizational unit in Google Workspace Admin. |

### User Aliases

| Action | Method | Description |
| --- | --- | --- |
| [Add User Alias](actions/add-user-alias.md) | POST | Adds a user alias in Google Workspace Admin. |
| [List User Aliases](actions/list-user-aliases.md) | GET | Retrieves a user's aliases from Google Workspace Admin. |
| [Remove User Alias](actions/remove-user-alias.md) | DELETE | Deletes a user alias from Google Workspace Admin. |

### User Photos

| Action | Method | Description |
| --- | --- | --- |
| [Get User Photo](actions/get-user-photo.md) | GET | Retrieves a user's photo from Google Workspace Admin. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Google Workspace Admin. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Google Workspace Admin. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Google Workspace Admin. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Google Workspace Admin. |
| [Undelete User](actions/undelete-user.md) | PUT | Restores a deleted user in Google Workspace Admin. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Google Workspace Admin. |

