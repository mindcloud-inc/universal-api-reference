# <img src="https://images.mindcloud.co/apps/icons/zammad_1776096891972.png" alt="Zammad logo" width="28" height="28"> Zammad: Universal API

Manage support tickets, users, and helpdesk workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zammad/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zammad.com
- **Vendor API docs:** https://docs.zammad.org/en/latest/api/intro.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Zammad. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Zammad. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Zammad. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Zammad. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Zammad. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in Zammad. |
| [Delete Organization](actions/delete-organization.md) | DELETE | Deletes an existing organization from Zammad. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Zammad. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Zammad. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Zammad. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a new role in Zammad. |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from Zammad. |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from Zammad. |
| [Update Role](actions/update-role.md) | PUT | Updates an existing role in Zammad. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Tags](actions/list-ticket-tags.md) | GET | Retrieves ticket tags from Zammad. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Delete Ticket](actions/delete-ticket.md) | DELETE | Deletes an existing ticket from Zammad. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from Zammad. |
| [Search Tickets](actions/search-tickets.md) | GET | Finds tickets in Zammad by search query. |

### Ticket Priority

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Priority](actions/get-ticket-priority.md) | GET | Retrieves a ticket priority from Zammad. |
| [List Ticket Priorities](actions/list-ticket-priorities.md) | GET | Retrieves ticket priorities from Zammad. |

### Ticket State

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket State](actions/get-ticket-state.md) | GET | Retrieves a ticket state from Zammad. |
| [List Ticket States](actions/list-ticket-states.md) | GET | Retrieves ticket states from Zammad. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Zammad. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Zammad. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Zammad. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Zammad. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Zammad. |

