# <img src="https://images.mindcloud.co/apps/icons/zendesk_1772651870185.png" alt="Zendesk logo" width="28" height="28"> Zendesk: Universal API

Manage tickets, answer customers, build help centers, and track service.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zendesk/latest
- **Category:** Support / Ticketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zendesk.com
- **Vendor API docs:** https://developer.zendesk.com/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Auditlog

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Audits](actions/list-ticket-audits.md) | GET | Retrieves audits for a Zendesk ticket. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Forms](actions/list-ticket-forms.md) | GET | Retrieves a list of Zendesk ticket forms. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Zendesk. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from Zendesk. |

### Groupmembership

| Action | Method | Description |
| --- | --- | --- |
| [Create Group Membership](actions/create-group-membership.md) | POST | Creates a new group membership in Zendesk. |
| [List Group Memberships](actions/list-group-memberships.md) | GET | Retrieves a list of group memberships from Zendesk. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in Zendesk. |
| [Delete Organization](actions/delete-organization.md) | DELETE | Deletes an existing organization from Zendesk. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Zendesk. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Zendesk. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Zendesk. |

### Organizationmembership

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Membership](actions/create-organization-membership.md) | POST | Creates a new organization membership in Zendesk. |
| [List Organization Memberships](actions/list-organization-memberships.md) | GET | Retrieves a list of organization memberships from Zendesk. |

### Searchresult

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds records in Zendesk by search query. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Zendesk. |
| [Delete Ticket](actions/delete-ticket.md) | DELETE | Deletes an existing ticket from Zendesk. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from Zendesk. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves a list of tickets from Zendesk. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in Zendesk. |

### Ticketcomment

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Comments](actions/list-ticket-comments.md) | GET | Retrieves comments for a Zendesk ticket. |

### Ticketfield

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Fields](actions/list-ticket-fields.md) | GET | Retrieves a list of Zendesk ticket fields. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Zendesk. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Zendesk. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Zendesk. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Zendesk. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Zendesk. |
| [Search Users](actions/search-users.md) | GET | Finds users in Zendesk by search query. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Zendesk. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET | Retrieves a list of views from Zendesk. |

### Viewexecution

| Action | Method | Description |
| --- | --- | --- |
| [Execute View](actions/execute-view.md) | GET | Retrieves results for a Zendesk view. |

