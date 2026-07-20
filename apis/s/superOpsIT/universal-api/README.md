# <img src="https://images.mindcloud.co/apps/icons/super-ops-it_1774303523735.png" alt="SuperOps IT logo" width="28" height="28"> SuperOps IT: Universal API

Manage IT tickets, assets, users, tasks, and sites

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/superOpsIT/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://superops.com
- **Vendor API docs:** https://developer.superops.com/it

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tickets](actions/list-tickets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Asset Software](actions/list-asset-software.md) | GET |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET |  |
| [Get Asset Summary](actions/get-asset-summary.md) | GET |  |
| [List Assets](actions/list-assets.md) | GET |  |
| [Update Asset](actions/update-asset.md) | PUT |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Conversation](actions/create-ticket-conversation.md) | POST |  |
| [List Ticket Conversations](actions/list-ticket-conversations.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST |  |
| [Get Site](actions/get-site.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |
| [Update Site](actions/update-site.md) | PUT |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Note](actions/create-ticket-note.md) | POST |  |
| [List Ticket Notes](actions/list-ticket-notes.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST |  |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [List Tickets](actions/list-tickets.md) | GET |  |
| [Update Ticket](actions/update-ticket.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

