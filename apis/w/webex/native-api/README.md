# Webex: Native API Reference

A consolidated summary of Webex's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://developer.webex.com/docs
- **API base URL:** `https://webexapis.com/v1`

## Authentication

### OAuth2

Connect a Webex OAuth integration created in the Webex developer portal.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://webexapis.com/v1/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://webexapis.com/v1/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `spark:all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://webexapis.com/v1/access_token.

[Official authentication documentation](https://developer.webex.com/create/docs/authentication)

## Pagination

Use `max` in the query string to set the page size (default 10; accepted range 1–100).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | `POST /meetings` | [docs](https://developer.webex.com/meeting/docs/api/v1/meetings/create-a-meeting) |
| [Create Membership](actions/create-membership.md) | `POST /memberships` | [docs](https://developer.webex.com/messaging/docs/api/v1/memberships/create-a-membership) |
| [Create Message](actions/create-message.md) | `POST /messages` | [docs](https://developer.webex.com/messaging/docs/api/v1/messages/create-a-message) |
| [Create Room](actions/create-room.md) | `POST /rooms` | [docs](https://developer.webex.com/messaging/docs/api/v1/rooms/create-a-room) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://developer.webex.com/messaging/docs/api/v1/teams/create-a-team) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developer.webex.com/messaging/docs/api/v1/webhooks/create-a-webhook) |
| [Delete Meeting](actions/delete-meeting.md) | `DELETE /meetings/:meetingId` | [docs](https://developer.webex.com/meeting/docs/api/v1/meetings/delete-a-meeting) |
| [Delete Membership](actions/delete-membership.md) | `DELETE /memberships/:membershipId` | [docs](https://developer.webex.com/messaging/docs/api/v1/memberships/delete-a-membership) |
| [Delete Message](actions/delete-message.md) | `DELETE /messages/:messageId` | [docs](https://developer.webex.com/messaging/docs/api/v1/messages/delete-a-message) |
| [Delete Room](actions/delete-room.md) | `DELETE /rooms/:roomId` | [docs](https://developer.webex.com/messaging/docs/api/v1/rooms/delete-a-room) |
| [Delete Team](actions/delete-team.md) | `DELETE /teams/:teamId` | [docs](https://developer.webex.com/messaging/docs/api/v1/teams/delete-a-team) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://developer.webex.com/messaging/docs/api/v1/webhooks/delete-a-webhook) |
| [Get Meeting](actions/get-meeting.md) | `GET /meetings/:meetingId` | [docs](https://developer.webex.com/meeting/docs/api/v1/meetings/get-a-meeting) |
| [Get Membership](actions/get-membership.md) | `GET /memberships/:membershipId` | [docs](https://developer.webex.com/messaging/docs/api/v1/memberships/get-membership-details) |
| [Get Message](actions/get-message.md) | `GET /messages/:messageId` | [docs](https://developer.webex.com/messaging/docs/api/v1/messages/get-message-details) |
| [Get My Own Details](actions/get-my-own-details.md) | `GET /people/me` | [docs](https://developer.webex.com/admin/docs/api/v1/people/get-my-own-details) |
| [Get Room](actions/get-room.md) | `GET /rooms/:roomId` | [docs](https://developer.webex.com/messaging/docs/api/v1/rooms/get-room-details) |
| [Get Team](actions/get-team.md) | `GET /teams/:teamId` | [docs](https://developer.webex.com/messaging/docs/api/v1/teams/get-team-details) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhookId` | [docs](https://developer.webex.com/messaging/docs/api/v1/webhooks/get-webhook-details) |
| [List Meetings](actions/list-meetings.md) | `GET /meetings` | [docs](https://developer.webex.com/meeting/docs/api/v1/meetings/list-meetings) |
| [List Memberships](actions/list-memberships.md) | `GET /memberships` | [docs](https://developer.webex.com/messaging/docs/api/v1/memberships/list-memberships) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://developer.webex.com/messaging/docs/api/v1/messages/list-messages) |
| [List Rooms](actions/list-rooms.md) | `GET /rooms` | [docs](https://developer.webex.com/messaging/docs/api/v1/rooms/list-rooms) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://developer.webex.com/messaging/docs/api/v1/teams/list-teams) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developer.webex.com/messaging/docs/api/v1/webhooks/list-webhooks) |
| [Update Meeting](actions/update-meeting.md) | `PUT /meetings/:meetingId` | [docs](https://developer.webex.com/meeting/docs/api/v1/meetings/update-a-meeting) |
| [Update Membership](actions/update-membership.md) | `PUT /memberships/:membershipId` | [docs](https://developer.webex.com/messaging/docs/api/v1/memberships/update-a-membership) |
| [Update Message](actions/update-message.md) | `PUT /messages/:messageId` | [docs](https://developer.webex.com/messaging/docs/api/v1/messages/update-a-message) |
| [Update Room](actions/update-room.md) | `PUT /rooms/:roomId` | [docs](https://developer.webex.com/messaging/docs/api/v1/rooms/update-a-room) |
| [Update Team](actions/update-team.md) | `PUT /teams/:teamId` | [docs](https://developer.webex.com/messaging/docs/api/v1/teams/update-a-team) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:webhookId` | [docs](https://developer.webex.com/messaging/docs/api/v1/webhooks/update-a-webhook) |
