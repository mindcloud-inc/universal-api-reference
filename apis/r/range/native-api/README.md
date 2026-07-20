# Range: Native API Reference

A consolidated summary of Range's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.range.co/docs/api
- **API base URL:** `https://api.range.co`

## Authentication

### Basic Auth

Authenticate with your Range API key using HTTP Basic auth. Use the API key as the username and leave the password blank.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.range.co/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | `POST /v1/teams` | [docs](https://www.range.co/docs/api#rpc-create-team) |
| [Delete Team Relation](actions/delete-team-relation.md) | `DELETE /v1/teams/:teamId/relations/:userId` | [docs](https://www.range.co/docs/api#rpc-delete-team-relation) |
| [Find User](actions/find-user.md) | `GET /v1/users/find` | [docs](https://www.range.co/docs/api#rpc-find-user) |
| [Get Auth User](actions/get-auth-user.md) | `GET /v1/users/auth-user` | [docs](https://www.range.co/docs/api#rpc-auth-user) |
| [Get Team](actions/get-team.md) | `GET /v1/teams/:teamId` | [docs](https://www.range.co/docs/api#rpc-read-team) |
| [Get User](actions/get-user.md) | `GET /v1/users/:userId` | [docs](https://www.range.co/docs/api#rpc-read-user) |
| [List Org Users](actions/list-org-users.md) | `GET /v1/orgs/:orgId/users` | [docs](https://www.range.co/docs/api#rpc-list-users) |
| [List Teams](actions/list-teams.md) | `GET /v1/teams` | [docs](https://www.range.co/docs/api#rpc-list-teams) |
| [List Updates](actions/list-updates.md) | `GET /v1/updates` | [docs](https://www.range.co/docs/api#rpc-list-updates) |
| [List User Teams](actions/list-user-teams.md) | `GET /v1/users/:userId/teams` | [docs](https://www.range.co/docs/api#rpc-list-teams) |
| [Record Activity](actions/record-activity.md) | `POST /v1/activity` | [docs](https://www.range.co/docs/api#rpc-record-interaction) |
| [Update Team Relation](actions/update-team-relation.md) | `PUT /v1/teams/:teamId/relations/:userId` | [docs](https://www.range.co/docs/api#rpc-update-team-relation) |
| [Update User Profile](actions/update-user-profile.md) | `PUT /v1/users/:userId/profile` | [docs](https://www.range.co/docs/api#rpc-update-user-profile) |
| [Update User State](actions/update-user-state.md) | `PUT /v1/users/:userId/state` | [docs](https://www.range.co/docs/api#rpc-update-user-state) |
