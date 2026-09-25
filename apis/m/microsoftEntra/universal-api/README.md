# <img src="https://images.mindcloud.co/apps/icons/official-entra-icon_1790271818554.png" alt="Microsoft Entra logo" width="28" height="28"> Microsoft Entra: Universal API

Manage Microsoft Entra users, groups, memberships, and directory data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftEntra/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/en-us/security/business/microsoft-entra
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Directory Object

| Action | Method | Description |
| --- | --- | --- |
| [List Group Memberships](actions/list-group-memberships.md) | GET |  |
| [List Group Transitive Memberships](actions/list-group-transitive-memberships.md) | GET |  |
| [List User Memberships](actions/list-user-memberships.md) | GET |  |
| [List User Owned Objects](actions/list-user-owned-objects.md) | GET |  |
| [List User Transitive Memberships](actions/list-user-transitive-memberships.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Group Member

| Action | Method | Description |
| --- | --- | --- |
| [Remove Group Member](actions/remove-group-member.md) | DELETE |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get User](actions/get-user.md) | GET |  |
| [Get User Manager](actions/get-user-manager.md) | GET |  |
| [List User Direct Reports](actions/list-user-direct-reports.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Remove User Manager](actions/remove-user-manager.md) | DELETE |  |
| [Set User Manager](actions/set-user-manager.md) | PUT |  |
| [Update User](actions/update-user.md) | PUT |  |

