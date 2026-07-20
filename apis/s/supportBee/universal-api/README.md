# <img src="https://images.mindcloud.co/apps/icons/support-bee_1774383129121.png" alt="SupportBee logo" width="28" height="28"> SupportBee: Universal API

SupportBee is a customer support help desk and shared inbox platform for managing tickets, replies, comments, teams, labels, and inbox workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/supportBee/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://supportbee.com
- **Vendor API docs:** https://supportbee.com/docs/api/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tickets](actions/list-tickets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a comment on a SupportBee ticket. |
| [List Ticket Comments](actions/list-ticket-comments.md) | GET | Retrieves comments for a SupportBee ticket. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from SupportBee. |

### Reply

| Action | Method | Description |
| --- | --- | --- |
| [Create Reply](actions/create-reply.md) | POST | Creates a reply on a SupportBee ticket. |
| [List Ticket Replies](actions/list-ticket-replies.md) | GET | Retrieves replies for a SupportBee ticket. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from SupportBee. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Add Label to Ticket](actions/add-label-to-ticket.md) | PUT | Adds a label to a SupportBee ticket. |
| [Archive Ticket](actions/archive-ticket.md) | PUT | Archives a ticket in SupportBee. |
| [Assign Ticket to Team](actions/assign-ticket-to-team.md) | PUT | Assigns a SupportBee ticket to a team. |
| [Assign Ticket to User](actions/assign-ticket-to-user.md) | PUT | Assigns a SupportBee ticket to a user. |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in SupportBee. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from SupportBee. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from SupportBee. |
| [Mark Ticket Answered](actions/mark-ticket-answered.md) | PUT | Marks a SupportBee ticket as answered. |
| [Mark Ticket as Spam](actions/mark-ticket-as-spam.md) | PUT | Marks a SupportBee ticket as spam. |
| [Mark Ticket Unanswered](actions/mark-ticket-unanswered.md) | PUT | Marks a SupportBee ticket as unanswered. |
| [Restore Ticket](actions/restore-ticket.md) | PUT | Restores a trashed SupportBee ticket. |
| [Search Tickets](actions/search-tickets.md) | GET | Finds tickets in SupportBee by search query. |
| [Trash Ticket](actions/trash-ticket.md) | PUT | Moves a SupportBee ticket to trash. |
| [Unarchive Ticket](actions/unarchive-ticket.md) | PUT | Unarchives a ticket in SupportBee. |
| [Unassign Ticket from Team](actions/unassign-ticket-from-team.md) | PUT | Unassigns a SupportBee ticket from its team. |
| [Unassign Ticket from User](actions/unassign-ticket-from-user.md) | PUT | Unassigns a SupportBee ticket from its user. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user or customer group from SupportBee. |
| [List Users](actions/list-users.md) | GET | Retrieves users and customer groups from SupportBee. |

