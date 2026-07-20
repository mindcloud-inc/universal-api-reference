# <img src="https://images.mindcloud.co/apps/icons/connect-256_1775166604882.png" alt="Zoho Connect logo" width="28" height="28"> Zoho Connect: Universal API

Zoho Connect is Zoho's workplace social network and collaboration platform for networks, groups, feeds, tasks, events, and people discovery.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoConnect/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/connect/
- **Vendor API docs:** https://www.zoho.com/connect/api/intro.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Networks](actions/get-all-networks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-networks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Add Member to a Board](actions/add-member-to-a-board.md) | POST | Adds members to a board in Zoho Connect. |
| [Create Board](actions/create-board.md) | POST | Creates a new board in Zoho Connect. |
| [Get Board Sections](actions/get-board-sections.md) | GET | Retrieves board sections from Zoho Connect. |
| [Get My Boards](actions/get-my-boards.md) | GET | Retrieves your boards from Zoho Connect. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST | Creates a new comment in Zoho Connect. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Event Invitees](actions/add-event-invitees.md) | POST | Adds invitees to an event in Zoho Connect. |
| [Add Event Reminder](actions/add-event-reminder.md) | POST | Adds a reminder to an event in Zoho Connect. |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Zoho Connect. |
| [Remove Event Reminder](actions/remove-event-reminder.md) | DELETE | Removes a reminder from a Zoho Connect event. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Zoho Connect. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Add User to a Group](actions/add-user-to-a-group.md) | POST | Adds users to a group in Zoho Connect. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Zoho Connect. |
| [Get All Groups](actions/get-all-groups.md) | GET | Retrieves all groups from Zoho Connect. |
| [Get User Groups](actions/get-user-groups.md) | GET | Retrieves a user's groups from Zoho Connect. |
| [Leave Group](actions/leave-group.md) | DELETE | Leaves a group in Zoho Connect. |

### Network Member

| Action | Method | Description |
| --- | --- | --- |
| [Get All Network Members](actions/get-all-network-members.md) | GET | Retrieves all network members from Zoho Connect. |

### Stream

| Action | Method | Description |
| --- | --- | --- |
| [Get My Feeds & Group Feeds](actions/get-my-feeds-group-feeds.md) | GET | Retrieves your feeds and group feeds from Zoho Connect. |
| [Get Single Feed](actions/get-single-feed.md) | GET | Retrieves a single feed from Zoho Connect. |
| [Get User Feed](actions/get-user-feed.md) | GET | Retrieves a user's feed from Zoho Connect. |
| [Start a Feed](actions/start-a-feed.md) | POST | Creates a new feed in Zoho Connect. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | PUT | Completes a task in Zoho Connect. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Zoho Connect. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Zoho Connect. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get All Networks](actions/get-all-networks.md) | GET | Retrieves all networks from Zoho Connect. |

