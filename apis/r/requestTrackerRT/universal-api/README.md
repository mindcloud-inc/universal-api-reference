# <img src="https://images.mindcloud.co/apps/icons/request-tracker-rt_1774457764784.png" alt="Request Tracker (RT) logo" width="28" height="28"> Request Tracker (RT): Universal API

Request Tracker (RT) is Best Practical's ticketing and help desk platform for managing requests, queues, users, groups, and support workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/requestTrackerRT/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://requesttracker.com/
- **Vendor API docs:** https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Queues](actions/list-queues.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/list-queues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Attachments](actions/get-ticket-attachments.md) | GET | Retrieves a ticket's attachments from Request Tracker. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Request Tracker. |
| [Get User Groups](actions/get-user-groups.md) | GET | Retrieves a user's groups from Request Tracker. |
| [Search Groups](actions/search-groups.md) | GET | Finds groups in Request Tracker. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Members](actions/get-group-members.md) | GET | Retrieves a group's members from Request Tracker. |

### Queue

| Action | Method | Description |
| --- | --- | --- |
| [Create Queue](actions/create-queue.md) | POST | Creates a new queue in Request Tracker. |
| [Get Queue](actions/get-queue.md) | GET | Retrieves a queue from Request Tracker. |
| [List Queues](actions/list-queues.md) | GET | Retrieves queues from Request Tracker. |
| [Search Queues](actions/search-queues.md) | GET | Finds queues in Request Tracker. |
| [Update Queue](actions/update-queue.md) | PUT | Updates an existing queue in Request Tracker. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Comment on Ticket](actions/comment-on-ticket.md) | PUT | Adds a comment to a ticket in Request Tracker. |
| [Correspond on Ticket](actions/correspond-on-ticket.md) | PUT | Adds a reply to a ticket in Request Tracker. |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Request Tracker. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from Request Tracker. |
| [Search Tickets](actions/search-tickets.md) | GET | Finds tickets in Request Tracker. |
| [Steal Ticket](actions/steal-ticket.md) | PUT | Reassigns a ticket to yourself in Request Tracker. |
| [Take Ticket](actions/take-ticket.md) | PUT | Assigns a ticket to yourself in Request Tracker. |
| [Untake Ticket](actions/untake-ticket.md) | PUT | Removes yourself from a ticket in Request Tracker. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in Request Tracker. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket History](actions/get-ticket-history.md) | GET | Retrieves a ticket's history from Request Tracker. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Request Tracker. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Request Tracker. |
| [Search Users](actions/search-users.md) | GET | Finds users in Request Tracker. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Request Tracker. |

