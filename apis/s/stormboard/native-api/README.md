# Stormboard: Native API Reference

A consolidated summary of Stormboard's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.stormboard.com/docs
- **API base URL:** `https://api.stormboard.com`

## Authentication

### API Key

Authenticate with a Stormboard account API key from the Account API tab.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.stormboard.com/docs/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Storm Invite](actions/accept-storm-invite.md) | `POST /storms/:storm_id/invite/accept` | [docs](https://api.stormboard.com/docs) |
| [Check Authentication](actions/check-authentication.md) | `GET /users/test` | [docs](https://api.stormboard.com/docs) |
| [Create Chat Message](actions/create-chat-message.md) | `POST /chat/:storm_id` | [docs](https://api.stormboard.com/docs) |
| [Create Comment](actions/create-comment.md) | `POST /ideas/:idea_id/comments` | [docs](https://api.stormboard.com/docs) |
| [Create Idea](actions/create-idea.md) | `POST /ideas` | [docs](https://api.stormboard.com/docs) |
| [Create Storm](actions/create-storm.md) | `POST /storms` | [docs](https://api.stormboard.com/docs) |
| [Decline Storm Invite](actions/decline-storm-invite.md) | `POST /storms/:storm_id/invite/decline` | [docs](https://api.stormboard.com/docs) |
| [Delete Idea](actions/delete-idea.md) | `DELETE /ideas/:idea_id` | [docs](https://api.stormboard.com/docs) |
| [Get Idea Data](actions/get-idea-data.md) | `GET /ideas/:idea_id` | [docs](https://api.stormboard.com/docs) |
| [Get Storm Access](actions/get-storm-access.md) | `GET /storms/:storm_id/access` | [docs](https://api.stormboard.com/docs) |
| [Get Storm Details](actions/get-storm-details.md) | `GET /storms/:storm_id` | [docs](https://api.stormboard.com/docs) |
| [Get User Profile](actions/get-user-profile.md) | `GET /users/profile` | [docs](https://api.stormboard.com/docs) |
| [Invite Participants](actions/invite-participants.md) | `POST /storms/:storm_id/invite` | [docs](https://api.stormboard.com/docs) |
| [Join Storm](actions/join-storm.md) | `POST /storms/join` | [docs](https://api.stormboard.com/docs) |
| [Leave Storm](actions/leave-storm.md) | `POST /storms/:storm_id/leave` | [docs](https://api.stormboard.com/docs) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /chat/:storm_id/list` | [docs](https://api.stormboard.com/docs) |
| [List Comments](actions/list-comments.md) | `GET /ideas/:idea_id/comments` | [docs](https://api.stormboard.com/docs) |
| [List Storm Ideas](actions/list-storm-ideas.md) | `GET /storms/:storm_id/ideas` | [docs](https://api.stormboard.com/docs) |
| [List Storm Invites](actions/list-storm-invites.md) | `GET /storms/invites` | [docs](https://api.stormboard.com/docs) |
| [List Storm Participants](actions/list-storm-participants.md) | `GET /storms/:storm_id/users` | [docs](https://api.stormboard.com/docs) |
| [List Storms](actions/list-storms.md) | `GET /storms/list` | [docs](https://api.stormboard.com/docs) |
| [Update Idea](actions/update-idea.md) | `PUT /ideas/:idea_id` | [docs](https://api.stormboard.com/docs) |
| [Update Idea Task](actions/update-idea-task.md) | `PUT /ideas/:idea_id/task` | [docs](https://api.stormboard.com/docs) |
| [Update Storm](actions/update-storm.md) | `PUT /storms/:storm_id` | [docs](https://api.stormboard.com/docs) |
