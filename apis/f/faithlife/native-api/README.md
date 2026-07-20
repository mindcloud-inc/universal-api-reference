# Faithlife: Native API Reference

A consolidated summary of Faithlife's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developer.faithlife.com/
- **API base URL:** `https://accountsapi.logos.com/v2`

## Authentication

### OAuth 1.0

### Credentials

- **Consumer Key:** `consumerKey` · required
- **Consumer Secret:** `consumerSecret` · required
- **Access Token:** `accessToken` · required
- **Token Secret:** `tokenSecret` · required
- **Realm:** `realm` · optional

OAuth 1.0a signs every request with the consumer key and secret plus the access token and token secret. Use an OAuth 1.0a client library to construct the `Authorization` header; the signature depends on the HTTP method, URL, and request parameters and should not be assembled as a static token.

[Official authentication documentation](https://developer.faithlife.com/)

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Invite To Group](actions/accept-invite-to-group.md) | `POST /invites/:inviteId/accept` | [docs](https://developer.faithlife.com/) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://developer.faithlife.com/) |
| [Delete Membership](actions/delete-membership.md) | `DELETE /memberships/:membershipId` | [docs](https://developer.faithlife.com/) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://developer.faithlife.com/) |
| [Get Group](actions/get-group.md) | `GET /groups/:groupId` | [docs](https://developer.faithlife.com/) |
| [Get Group Newsfeed](actions/get-group-newsfeed.md) | `GET https://api.faithlife.com/community/v2/groups/:groupId/newsfeed` | [docs](https://developer.faithlife.com/) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://developer.faithlife.com/) |
| [Invite Users To Group](actions/invite-users-to-group.md) | `POST /groups/:groupId/invites` | [docs](https://developer.faithlife.com/) |
| [List Group Invites](actions/list-group-invites.md) | `GET /groups/:groupId/invites` | [docs](https://developer.faithlife.com/) |
| [List Groups For User](actions/list-groups-for-user.md) | `GET /users/:userId/groups` | [docs](https://developer.faithlife.com/) |
| [List My Invites](actions/list-my-invites.md) | `GET /invites` | [docs](https://developer.faithlife.com/) |
| [Search Groups](actions/search-groups.md) | `GET /groups` | [docs](https://developer.faithlife.com/) |
| [Search Users](actions/search-users.md) | `GET /users` | [docs](https://developer.faithlife.com/) |
