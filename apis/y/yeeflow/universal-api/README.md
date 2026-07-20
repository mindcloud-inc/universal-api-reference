# <img src="https://images.mindcloud.co/apps/icons/64e86b028c74f4adb9c90e79-webclip-256x256_1774979958051.png" alt="Yeeflow logo" width="28" height="28"> Yeeflow: Universal API

Yeeflow is a no-code workflow automation and work management platform with APIs for users, departments, locations, groups, positions, workflows, service portal, files, agents, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yeeflow/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.yeeflow.com
- **Vendor API docs:** https://developer.yeeflow.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Departments](actions/list-departments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/list-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | POST |  |
| [Delete Department](actions/delete-department.md) | DELETE |  |
| [List Departments](actions/list-departments.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Users To Group](actions/add-users-to-group.md) | PUT |  |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Remove Users From Group](actions/remove-users-from-group.md) | PUT |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [Delete Location](actions/delete-location.md) | DELETE |  |
| [Get Location](actions/get-location.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |
| [Update Location](actions/update-location.md) | PUT |  |

### Positions

| Action | Method | Description |
| --- | --- | --- |
| [Assign Users To Position](actions/assign-users-to-position.md) | PUT |  |
| [Create Position](actions/create-position.md) | POST |  |
| [Delete Position](actions/delete-position.md) | DELETE |  |
| [Get Position Assignments](actions/get-position-assignments.md) | GET |  |
| [List Positions](actions/list-positions.md) | GET |  |
| [Remove Users From Position](actions/remove-users-from-position.md) | PUT |  |
| [Update Position](actions/update-position.md) | PUT |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Pending Tasks](actions/list-pending-tasks.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Disable User](actions/disable-user.md) | PUT |  |
| [Enable User](actions/enable-user.md) | PUT |  |
| [Get User](actions/get-user.md) | GET |  |
| [Get User By Account ID](actions/get-user-by-account-id.md) | GET |  |
| [List Group Users](actions/list-group-users.md) | GET |  |
| [Search Users](actions/search-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Delegation](actions/create-delegation.md) | POST |  |
| [Delete Delegation](actions/delete-delegation.md) | DELETE |  |
| [Disable Delegation](actions/disable-delegation.md) | PUT |  |
| [Enable Delegation](actions/enable-delegation.md) | PUT |  |
| [Get Delegation](actions/get-delegation.md) | GET |  |
| [List Delegations](actions/list-delegations.md) | GET |  |
| [Update Delegation](actions/update-delegation.md) | PUT |  |

