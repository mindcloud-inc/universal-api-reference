# Zoho Connect: Native API Reference

A consolidated summary of Zoho Connect's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/connect/api/intro.html
- **API base URL:** `https://connect.zoho.com`

## Authentication

### OAuth 2.0

Connect Zoho Connect with a Zoho OAuth 2.0 client and authorize the required Zoho Connect scopes.

### Credentials

- **Network ID:** `networkId` · required · Enter the Zoho Connect Network ID (Scope ID). You can find it in any group under Settings > Developer Info.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `zohopulse.networklist.READ zohopulse.userDetail.READ zohopulse.feedList.READ zohopulse.feedList.CREATE zohopulse.tasks.READ zohopulse.tasks.CREATE zohopulse.tasks.UPDATE zohopulse.events.CREATE zohopulse.events.UPDATE zohopulse.events.DELETE zohopulse.grouplist.CREATE zohopulse.grouplist.DELETE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/connect/api/authentication.html)

## API conventions

Response data is read from `allScopes.scopes`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | `POST /pulse/api/v2/addComment` | [docs](https://www.zoho.com/connect/api/add-comment.html) |
| [Add Event Invitees](actions/add-event-invitees.md) | `POST /pulse/api/addEventInvitees` | [docs](https://www.zoho.com/connect/api/add-event-invitees.html) |
| [Add Event Reminder](actions/add-event-reminder.md) | `POST /pulse/api/addEventReminder` | [docs](https://www.zoho.com/connect/api/add-event-reminder.html) |
| [Add Member to a Board](actions/add-member-to-a-board.md) | `POST /pulse/api/addMembersToBoard` | [docs](https://www.zoho.com/connect/api/add-member-to-board.html) |
| [Add User to a Group](actions/add-user-to-a-group.md) | `POST /pulse/api/addUsersToGroup` | [docs](https://www.zoho.com/connect/api/add-user-to-group.html) |
| [Complete Task](actions/complete-task.md) | `POST /pulse/api/completeTask` | [docs](https://www.zoho.com/connect/api/complete-task.html) |
| [Create Board](actions/create-board.md) | `POST /pulse/api/addBoard` | [docs](https://www.zoho.com/connect/api/create-board.html) |
| [Create Event](actions/create-event.md) | `POST /pulse/api/addEvent` | [docs](https://www.zoho.com/connect/api/create-event.html) |
| [Create Group](actions/create-group.md) | `POST /pulse/api/addGroup` | [docs](https://www.zoho.com/connect/api/create-group.html) |
| [Create Task](actions/create-task.md) | `POST /pulse/api/addTask` | [docs](https://www.zoho.com/connect/api/create-task.html) |
| [Get All Groups](actions/get-all-groups.md) | `GET /pulse/api/allGroups` | [docs](https://www.zoho.com/connect/api/get-all-groups.html) |
| [Get All Network Members](actions/get-all-network-members.md) | `GET /pulse/api/orgMembers` | [docs](https://www.zoho.com/connect/api/get-all-network-members.html) |
| [Get All Networks](actions/get-all-networks.md) | `GET /pulse/api/allScopes` | [docs](https://www.zoho.com/connect/api/get-all-networks.html) |
| [Get Board Sections](actions/get-board-sections.md) | `GET /pulse/api/boardSections` | [docs](https://www.zoho.com/connect/api/get-board-sections.html) |
| [Get My Boards](actions/get-my-boards.md) | `GET /pulse/api/myBoards` | [docs](https://www.zoho.com/connect/api/get-my-boards.html) |
| [Get My Feeds & Group Feeds](actions/get-my-feeds-group-feeds.md) | `GET /pulse/api/getLatestStreams` | [docs](https://www.zoho.com/connect/api/get-my-feed-group-feed.html) |
| [Get Single Feed](actions/get-single-feed.md) | `GET /pulse/api/v1/singleStream` | [docs](https://www.zoho.com/connect/api/get-single-feed.html) |
| [Get User Feed](actions/get-user-feed.md) | `GET /pulse/api/v1/userStreams` | [docs](https://www.zoho.com/connect/api/get-user-feed.html) |
| [Get User Groups](actions/get-user-groups.md) | `GET /pulse/api/userGroups` | [docs](https://www.zoho.com/connect/api/get-user-groups.html) |
| [Leave Group](actions/leave-group.md) | `DELETE /pulse/api/leaveGroup` | [docs](https://www.zoho.com/connect/api/leave-group.html) |
| [Remove Event Reminder](actions/remove-event-reminder.md) | `DELETE /pulse/api/deleteEventReminder` | [docs](https://www.zoho.com/connect/api/remove-event-reminder.html) |
| [Start a Feed](actions/start-a-feed.md) | `POST /pulse/api/v2/addStream` | [docs](https://www.zoho.com/connect/api/start-a-feed.html) |
| [Update Event](actions/update-event.md) | `POST /pulse/api/updateEvent` | [docs](https://www.zoho.com/connect/api/update-event.html) |
| [Update Task](actions/update-task.md) | `POST /pulse/api/updateTask` | [docs](https://www.zoho.com/connect/api/update-task.html) |
